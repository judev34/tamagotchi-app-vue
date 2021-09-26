<template>
    <div>
        <div class="pet-card">
            <h3>Pet Name</h3>
            <div class="container-progress-bar">
                <div class="progress-bar" id="stat-food">
                    <div></div>
                </div>
                <div class="progress-bar" id="stat-sleep">
                    <div></div>
                </div>
                <div class="progress-bar" id="stat-play">
                    <div></div>
                </div>
            </div>
            
        </div>
    </div>    
</template>

<script>
export default {
    
}
</script>

<style scoped>

.container-progress-bar {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.progress-bar {
    margin: 20px 0;
    background-color: lightgrey;
    width: 300px;
    height: 20px;
}

</style>