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
    
        <!-- Boost -->
        <div class='centerBoost'>
            <slot name="boost"/>
        </div>
        
    </section>
</main>

<style>
    section{
		width: 246px;
        height: 55px;
		display: grid;
		grid-template-columns: 1fr 3fr 1fr;
		padding-left: 11px;
		padding-right: 11px;
        border-radius: 7px;
		margin-bottom: 8px;
        background: rgb(143,78,112);
        background: linear-gradient(95deg, rgba(143,78,112,1) 0%, rgba(107,66,114,1) 100%);
	}

    .centerCover {
		text-align: left;
        display: flex;
        flex-flow: column;
        justify-content: center;
	}

    .centerInfo {
        text-align: left;
        display: flex;
        flex-flow: column;
        justify-content: center;
        line-height: 1.5;
    }

    .centerBoost {
		text-align: right;
        display: flex;
        flex-flow: column;
        justify-content: center;
	}
</style>
