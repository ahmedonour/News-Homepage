<script>
    export let src;
    export let num;
    export let h_one;
    export let parghraph;
</script>
<main>
    <img src={src} alt="small images">
    <p class="num">{num}</p>
    <h1>{h_one}</h1>
    <p class="praghraph">{parghraph}</p>
</main>
<style>
    main{
        display: grid;
        
        align-items: flex-start;
        grid-template-columns: repeat(2 , .5fr);
        grid-template-rows: repeat(3, 1fr);
        margin-bottom: 2rem;
        width: 90vw;
    }
    img{
        width: 100px;
        grid-row: 1 / 4;
        grid-column: 1;
    }
    .num{
        grid-row: 1;
        grid-column: 2;
        font-size: 2rem;
        font-weight: 600;
        font-family: var(--ff-inter);
        color: var(--Dark-grayish-blue);
    }
    h1{
        font-size: 1rem;
        grid-row: 2;
        grid-column: 2;
        font-family: var(--ff-inter);

        color: var(--Very-dark-blue);
    }
    .praghraph{
        font-size: .8rem;
        grid-row: 3;
        grid-column: 2;
        font-family: var(--ff-inter);

        color: var(--Grayish-blue);
    }
    @media screen and (min-width: 1024px){
        main{
            width: 30%;
            
        }
    }
</style>