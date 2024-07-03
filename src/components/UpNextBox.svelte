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
		width: 352px;
        height: 78px;
		display: grid;
		grid-template-columns: 1fr 3fr 1fr;
		padding-left: 16px;
		padding-right: 16px;
        border-radius: 10px;
		margin-bottom: 12px;
        background: rgb(117,116,112);
        background: linear-gradient(95deg, rgba(117,116,112,1) 0%, rgba(93,92,88,1) 100%);
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
