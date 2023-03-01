<template>
    <div class="main-mail-content">
        <div class="left-mail-content">
            <div class="head">
                <h1 class="page-title">Mails</h1>
                <MailToolbar />
            </div>
            <div class="mails">
                <div class="single-mail">
                    <input type="checkbox" v-model="checkAll" id="1" class="checkbox-custom mail-checker" />
                    <div class="mail-subject">Betreff</div>
                    <div class="mail-consignor">Absender</div>
                    <div class="mail-date">Datum</div>
                </div>
                <div class="single-mail">
                    <input type="checkbox" v-model="checkAll" id="2" class="checkbox-custom mail-checker" />
                    <div class="mail-subject">Betreff</div>
                    <div class="mail-consignor">Absender</div>
                    <div class="mail-date">Datum</div>
                </div>
                <div class="single-mail">
                    <input type="checkbox" v-model="checkAll" id="3" class="checkbox-custom mail-checker" />
                    <div class="mail-subject">Betreff</div>
                    <div class="mail-consignor">Absender</div>
                    <div class="mail-date">Datum</div>
                </div>
                <div class="single-mail">
                    <input type="checkbox" v-model="checkAll" id="4" class="checkbox-custom mail-checker" />
                    <div class="mail-subject">Betreff</div>
                    <div class="mail-consignor">Absender</div>
                    <div class="mail-date">Datum</div>
                </div>
                <div class="single-mail">
                    <input type="checkbox" v-model="checkAll" id="5" class="checkbox-custom mail-checker" />
                    <div class="mail-subject">Betreff</div>
                    <div class="mail-consignor">Absender</div>
                    <div class="mail-date">Datum</div>
                </div>
            </div>
        </div>
        <div class="right-mail-content">
            <input alt="Mail suchen" onfocus="this.value=''" value="Mail suchen" type="text" id="mail-search" name="mail-search" />
            <div class="main-directories">
                <a href="/">
                    <h2>Posteingang:</h2>
                </a>
                <ul>
                    <li>
                        <a href="/">Entwurf</a>
                    </li>
                    <li>
                        <a href="/">Gesendet</a>
                    </li>
                    <li>
                        <a href="/">Archiv</a>
                    </li>
                    <li>
                        <a href="/">Spam</a>
                    </li>
                    <li>
                        <a href="/">Papierkorb</a>
                    </li>
                </ul>
            </div>
            <div class="additional-directories">
                <h2>Ordner:</h2>
                <ul>
                    <li>
                        <a href="/">Pätzoldt</a>
                    </li>
                    <li>
                        <a href="/">1. Semester</a>
                    </li>
                    <li>
                        <a href="/">2. Semester</a>
                    </li>
                    <li>
                        <a href="/">3. Semester</a>
                    </li>
                    <li>
                        <a href="/">4. Semester</a>
                    </li>
                    <li>
                        <a href="/">5. Semester</a>
                    </li>
                    <li>
                        <a href="/">6. Semester</a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
import MailToolbar from '~/components/MailToolbar.vue';
import ScheduleList from '~/components/ScheduleList.vue';

const layout = "mail";

export default {
    components: {
        MailToolbar,
        ScheduleList,
    },
    layout: "mail",
    name: "MailPage",
}
</script>

<style lang="scss">
/* Dark Theme Styling */
.theme--dark .head {
    background-color: $color-dark-mode;
}

.theme--dark .mail-subject,
.theme--dark .mail-consignor,
.theme--dark .mail-date {
    color: $color-dark-mode;
}

.theme--dark #mail-search a,
.theme--dark .main-directories,
.theme--dark .main-directories a,
.theme--dark .additional-directories,
.theme--dark .additional-directories a {
    color: $color-white;
    text-decoration: none;
}

/* Light Theme Styling */
.theme--light .mail-subject,
.theme--light .mail-consignor,
.theme--light .mail-date {
    color: $color-dark-mode;
}

.theme--light #mail-search a,
.theme--light .main-directories,
.theme--light .main-directories a,
.theme--light .additional-directories,
.theme--light .additional-directories a {
    color: $color-white;
    text-decoration: none;
}

/* General Mobile Styling */


/* General Desktop Styling */
.main-mail-content {
    display: flex;
    flex-direction: row;
}

.left-mail-content {
    display: flex;
    flex-direction: column;
    width: 80vw;
}

.head {
    display: flex;
    flex-direction: row;
    height: 10vh;
    width: 80vw;
    padding: 1rem;
    border-bottom: 2px solid $color-hwr-red;
}

.mails {
    display: flex;
    flex-direction: column;
    height: 100%;
}

.single-mail {
    display: flex;
    flex-direction: row;
    align-items: center;
    height: 3rem;
    border-bottom: 1px solid $color-white;
    background-color: $color-grey-mail;
}

.mail-checker {
    width: 5%;
    margin-left: 2rem;
}

.mail-subject {
    width: 40%;
}

.mail-consignor {
    width: 45%;
}

.mail-date {
    width: 10%;
}

.mail-subject,
.mail-consignor,
.mail-date {
    padding-left: 0.5rem;
}

.page-title {
    padding-left: 2rem;
    align-self: center;
    width: 15vw;
}

.right-mail-content {
    display: flex;
    flex-direction: column;
    padding: 1.5rem;
    height: 100vh;
    width: 100vw;
    background-color: $color-hwr-red;
}

#mail-search a,
.main-directories,
.main-directories a,
.additional-directories,
.additional-directories a {
    color: $color-white;
    text-decoration: none;
}


#mail-search {
    background-color: $color-white;
}

.main-directories,
.additional-directories {
    margin: 1rem 0;
}

.main-directories li,
.additional-directories li {
    margin-top: 0.5rem;
    margin-bottom: 1.5rem;
}

.v-btn {
    border: 1px solid $color-hwr-red;
}
</style>
