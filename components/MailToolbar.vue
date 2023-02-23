<template>
  <div>
    <div>
      <template>
        <v-row>
          <div class="checkBox">
            <input type="checkbox" v-model="checkAll" class="checkbox-custom" />
          </div>

          <div class="new">
            <v-dialog v-model="dialog" persistent width="1024">
              <template v-slot:activator="{ props }">
                <v-btn v-bind="props" @click="dialog = true">
                  <v-icon>mdi-file-plus @click="dialog = true"</v-icon>Verfassen
                </v-btn>
              </template>
              <v-card>
                <v-card-title>
                  <div class="emailTitle">Send Email</div>
                </v-card-title>
                <v-card-text>
                  <v-container>
                    <template>
                      <div class="container">
                        <form @submit.prevent="saveData()">
                          <form @submit.prevent="sendEmail">
                            <label>Email</label>
                            <input
                              type="email"
                              v-model="email"
                              name="email"
                              placeholder="To"
                            />

                            <label>CC</label>
                            <input
                              type="email"
                              v-model="email"
                              name="email"
                              placeholder="CC"
                            />

                            <label>Subject</label>
                            <input
                              type="text"
                              v-model="name"
                              name="name"
                              placeholder="Subject"
                            />

                            <label>Message</label>
                            <textarea
                              name="message"
                              v-model="message"
                              cols="30"
                              rows="5"
                              placeholder="Message"
                            >
                            </textarea>

                            <input type="submit" value="Send" />
                          </form>
                        </form>
                      </div>
                    </template>
                  </v-container>
                  <small>*indicates required field</small>
                </v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn
                    color="blue-darken-1"
                    variant="text"
                    @click="dialog = false"
                  >
                    Close
                  </v-btn>
                  <v-btn
                    color="blue-darken-1"
                    variant="text"
                    @click="dialog = false"
                  >
                    Save
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-dialog>
          </div>

          <div>
            <v-btn variant="flat"
              ><v-icon>mdi-folder-zip</v-icon> Archivieren
            </v-btn>
          </div>

          <div>
            <v-btn variant="tonal"
              ><v-icon>mdi-close-octagon</v-icon>Spam</v-btn
            >
          </div>

          <div>
            <v-btn variant="tonal"
              ><v-icon>mdi-folder-move</v-icon>Verschieben</v-btn
            >
          </div>
          <div>
            <v-btn variant="tonal"
              ><v-icon>mdi-delete-forever</v-icon>Löschen</v-btn
            >
          </div>
          <div class="menu">
            <v-menu bottom left>
              <template v-slot:activator="{ on, attrs }">
                <v-btn v-bind="attrs" v-on="on" color="primary" icon>
                  <v-icon>mdi-dots-vertical</v-icon>
                </v-btn>
              </template>

              <v-list>
                <v-list-item
                  v-for="(item, index) in options"
                  :key="index"
                  @click="handleClick(index)"
                >
                  <v-list-item-icon>
                    <v-icon v-text="item.icon"></v-icon>
                  </v-list-item-icon>
                  <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>
          </div>
        </v-row>
      </template>
    </div>
  </div>
</template>

<script>


export default {


  data: () => ({


	name: '',
	email: '',
	message: '',
    dialog: false,

    items: [
      {
        title: "Click Me"
      },
      {
        title: "Click Me"
      },
      {
        title: "Click Me"
      },
      {
        title: "Click Me 2"
      }
    ],
    select: [
      { text: "State 1" },
      { text: "State 2" },
      { text: "State 3" },
      { text: "State 4" },
      { text: "State 5" },
      { text: "State 6" },
      { text: "State 7" }
    ],
    options: [
      {
        title: "Edit",
        icon: "mdi-pencil",
        click() {
          console.log("edit");
        }
      },
      {
        title: "Due Date",
        icon: "mdi-calendar",
        click() {
          console.log("due date");
        }
      },
      {
        title: "Delete",
        icon: "mdi-delete",
        click() {
          // this.$store.dispatch('deleteTask', 1)
          console.log("Logout");
        }
      }
    ]
  }),
  methods: {

    handleClick(index) {
      this.options[index].click.call(this);
    },

	sendEmail(e) {
      try {
        sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', e.target, 'YOUR_USER_ID', {
          name: this.name,
          email: this.email,
          message: this.message
        })

      } catch (err) {
           if (err instanceof ReferenceError) {
            alert( "JSON Error: " + err.message );
           } else {
            throw err; // rethrow
           }
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  }
};
</script>

<style>
.checkbox-custom {
  width: 2rem;
  height: 2rem;
  float: left;
  margin-right: 2rem;
}

.list {
  width: 100px;
  height: 100px;
  display: block;
}

.new {
  margin-right: 5rem;
}

.menu {
  margin-left: 3rem;
}

.toolbar {
  background-color: #363636;
}

.v-btn > .v-btn__content .v-icon {
  font-size: 2.1rem;
  color: #d50b2e;
}

label {
  float: left;
}
input[type="text"],
[type="email"],
textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}

input[type="submit"] {
  background-color: #4caf50;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type="submit"]:hover {
  background-color: #b8c7b9;
}
</style>
