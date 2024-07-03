<main>
    <section>
        <!-- Album Cover -->
        <div class='centerCover'>
            <slot name="cover"/>
        </div>
    
        <!-- Song Info -->
        <div class='centerInfo'>
            <slot name="song"/>
            <slot name="album"/>
        </div>
    
        <!-- Cooldown -->
        <div class='centerCooldown'>
            <slot name="cooldown"/>
        </div>
        
    </section>
</main>

<style>
    section{
		width: 352px;
        height: 78px;
		display: grid;
		grid-template-columns: 1fr 3fr 1fr;
		padding-left: 16px;
		padding-right: 16px;
        border-radius: 10px;
		margin-bottom: 12px;
        background: #50504d;
	}

    .centerCover {
        opacity: 30%;
		text-align: left;
        display: flex;
        flex-flow: column;
        justify-content: center;
	}

    .centerInfo {
        opacity: 30%;
        text-align: left;
        display: flex;
        flex-flow: column;
        justify-content: center;
        line-height: 1.5;
    }

    .centerCooldown {
		text-align: right;
        display: flex;
        flex-flow: column;
        justify-content: center;
	}
</style>