<template>
    <div class="password-recovery-panel">
        <div class="password-recovery-panel-top">
            <h1 class="first-title"> 
                HWR Student Portal 
            </h1>
            <img class="bear-image" src="~/assets/images/Bear.png">
            <h2 class="second-title"> 
                Wiederherstellung 
            </h2>
            <h3 class="third-title"> 
                des Benutzernamens 
            </h3>
        </div>
    </div>
</template>

<style>
.password-recovery-panel {
    width: 40%;
    height: 60%;
    padding: 50px;
    margin-top: 5%;
    margin-bottom: auto;
    display: flex;
    flex-direction: column;
    align-self: center;
    border: 1px solid #D50B2E;
    border-radius: 15px;
}

.password-recovery-panel-top {
    display: flex;
    flex-direction: column;
    align-self: center;
}

.first-title {
    margin-bottom: 30px;
    color: #D50B2E;
}

.bear-image {
    width: 45%;
    height: 60%;
    align-self: center;
}

.second-title {
    align-self: center;
    margin-bottom: 15px;
}

.third-title {
    align-self: center;
    margin-bottom: 30px;
}

.password-recovery-panel-middle {
    display: flex;
    flex-direction: column;
}

.password-recovery-input {
    background-color: #fff;
    border: 1px solid #D50B2E;
    width: 80%;
    align-self: center;
}

.forgot-password-link {
    margin-top: 10px;
    margin-bottom: 30px;
}

.password-recovery-panel-bottom {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 2%;
    justify-content: center;
}

.send-recovery-button {
    width: 49%;
    margin-top: 30px;
    height: 40px !important;
}
</style>