<template>
    <figure> 
        <div class="logos_SM">
            <a href="https://www.linkedin.com/in/raynaud-isabelle/" target="_blank"><img src="../assets/images/linkedin.png" alt="Logo LinkedIn"></a>
            <a href="https://github.com/IsaRaynaud" target="_blank"><img src="../assets/images/github.png" alt="Logo Github"></a>
        </div>

        <p id="update">Dernière mise à jour le <time datetime="2024-05-17">17 mai 2024</time>.</p>
    </figure>
</template>

<style scoped>
figure{
        background-color: #0A080C ;
        padding: 30px 30px 30px 15px;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 2.5rem;
      }

.logos_SM{
    display: flex;
    flex-direction: row;
    justify-content: center;
}

.logos_SM:hover{
    cursor: pointer;
}

#update{
    color: white;
    font-size: 0.8em;
}
</style>