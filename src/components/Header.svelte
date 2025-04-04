<script>
    // You can import your logo here if needed
    import logo from '../assets/Black_White_Minimal_Simple_Modern_Creative_Studio_Ego_Logo__2_-removebg-preview.png';
</script>

<style>
    header {
        
        width: 100%;
        height: 200px;
        margin-top: 20px;
        position: fixed;
        top: 0;
        left: 0;
        display: flex;
        justify-content: center;
        z-index: 1000;
        }

    img {
        width: 400px;
        height: auto;
        object-fit: cover;
        
    }
</style>

<header>
    <img src={logo} alt="Logo" />
</header>