<template>
    <section class="hero-wrapper">
        <div class="hero-imgs">
            <img src="../assets/image-mockups.png" alt="">
        </div>
        
        <div class="hero-text">
            <h1>Next generation digital banking</h1>
            <p>Take your financial life online. Your Easybank account will be a one-stop-shop 
  for spending, saving, budgeting, investing, and much more.</p>
            <button>Request Invite</button>
        </div>
    </section>
</template>

<script setup>

</script>

<style scoped>
section img {
    max-width: 100%;
}
section .hero-imgs {
    background-image: url(../assets/bg-intro-mobile.svg);
    background-repeat: no-repeat;
    background-size: contain;
	background-position-y: top -50px;
	overflow: hidden;
}
section .hero-imgs img {
	position: relative;
	top: -140px;
}
section .hero-text {
	position: relative;
	margin-top: -40%;
    padding: 1rem 2rem 5.5rem;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
}
section .hero-text h1 {
    color: var(--Dark-Blue);
    margin-bottom: 1.5rem;
    font-size: xx-large;
}
section .hero-text p {
    margin-bottom: 2rem;
    color: var(--Grayish-Blue);
}
section .hero-text button {
    border: none;
    border-radius: 5rem;
    background: linear-gradient(to right, var(--Lime-Green), var(--Bright-Cyan));
    color: var(--White);
    padding: 0.75rem 2rem;
    font-weight: 700;
    font-family: 'Public Sans';
}
</style>