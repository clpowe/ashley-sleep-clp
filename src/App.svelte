<script>
  import Hero from './lib/CLP-HERO/CLPHero.svelte'
  import ShopBy from './lib/ShopBy.svelte'
  import Marquee from './lib/Marquee.svelte'
  import Corporate from './lib/Corporate.svelte'
  import Ad from './lib/Ad.svelte'

  const hero = {
    title:'for your best rest',
    text:'With three different mattress lines designed to meet your comfort needs and your budget, every goodnight is followed by a great morning.',
    link:'',
    ariaLabel:'',
    altText:'',
    desktopImg:'',
    tabletImg:'',
    mobileImg:''
  }

  const shopby = [
    {
        id: 1,
        heading: 'shop by size',
        list: [
          {
            id: 1,
            icon:'',
            text:'TWIN',
            link:'',
            ariaLabel:'',
          },
          {
            id: 2,
            icon:'',
            text:'TWIN XL',
            link:'',
            ariaLabel:'',
          },
          {
            id: 3,
            icon:'',
            text:'FULL',
            link:'',
            ariaLabel:'',
          },
          {
            id: 4,
            icon:'',
            text:'QUEEN',
            link:'',
            ariaLabel:'',
          },
          {
            id: 5,
            icon:'',
            text:'KING',
            link:'',
            ariaLabel:'',
          },
          {
            id: 6,
            icon:'',
            text:'CALIFORNIA KING',
            link:'',
            ariaLabel:'',
          },
        ]
    },
    { 
        id: 2,
        heading: 'shop by comfort',
        list:[
          {
            id: 1,
            icon:'',
            text:'FIRM',
            link:'',
            ariaLabel:'',
          },
          {
            id: 2,
            icon:'',
            text:'MEDIUM',
            link:'',
            ariaLabel:'',
          },
          {
            id: 3,
            icon:'',
            text:'PLUSH',
            link:'',
            ariaLabel:'',
          },
          {
            id: 4,
            icon:'',
            text:'ULTRA PLUSH',
            link:'',
            ariaLabel:'',
          },
        ]
    },
    {
        id: 3,
        heading: 'shop by type',
        list:[
          {
            id: 1,
            icon:'',
            text:'MEMORY FOAM',
            link:'',
            ariaLabel:'',
          },
          {
            id: 2,
            icon:'',
            text:'HYBRID',
            link:'',
            ariaLabel:'',
          },
          {
            id: 3,
            icon:'',
            text:'INNERSPRING',
            link:'',
            ariaLabel:'',
          }
        ]
    }
  ]

  const marquees = [
    {
      id: 1,
      mainImg:'',
      mobileImg: '',
      altText:'',
      logo:'',
      mainText:'Explore explore our most affordable line of mattresses.',
      link:'',
      ariaLabel:'',
      variant:'essentials',
      list:[
        {
          id: 1,
          icon:'',
          text:'FIT FOR YOUR NEEDS'
        },
        {
          id: 2,
          icon:'',
          text:'CHOICE OF COMFORT'
        },
        {
          id: 3,
          icon:'',
          text:'MATTRESS IN A BOX'
        }
      ]
    },
    {
      id: 2,
      mainImg:'',
      mobileImg: '',
      altText:'',
      logo:'',
      mainText:'With more convenience and comfort, bedtime will feel even better.',
      link:'',
      ariaLabel:'',
      variant:'gruve',
      list:[
        {
          id: 1,
          icon:'',
          text:'COOLING'
        },
        {
          id: 2,
          icon:'',
          text:'HYPOALLERGENIC'
        },
        {
          id: 3,
          icon:'',
          text:'CHARCOAL + GREEN TEA INFUSED'
        }
      ]
    },
    {
      id: 3,
      mainImg:'',
      mobileImg: '',
      altText:'',
      logo:'',
      mainText:'Made with the highest quality materials, you can sleep in luxury without the luxury price tag.',
      link:'',
      variant:'align',
      list:[
        {
          id: 1,
          icon:'',
          text:'COOLING'
        },
        {
          id: 2,
          icon:'',
          text:'COPPER-INFUSED MEMORY FOAM'
        },
        {
          id: 3,
          icon:'',
          text:'CHARCOAL + GREEN TEA INFUSED'
        }
      ]
    },
  ]

  const corporate = [
    {
      icon:'',
      title:'financing options',
      text:'The freedom to pay your way',
      link:'',
      ariaLabel:'',
    },
    {
      icon:'',
      title:'special delivery',
      text:'From free shipping to premium delivery, there’s an option for everyone',
      link:'',
      ariaLabel:'',
    },
    {
      icon:'',
      title:'10-year warranty',
      text:'Sleep better knowing you’re always covered.* *Available on most mattresses',
      link:'',
      ariaLabel:'',
    },
    {
      icon:'',
      title:'rest assured',
      text:'All of our mattress are hypoallergenic and CertiPUR-US® certified',
      link:'',
      ariaLabel:'',
    },
  ]

  const ad = {
    img:'',
    altText:'',
    headline:'GIVING THE GIFT OF BETTER SLEEP',
    body:'For every mattress sold as Ashley, a portion of the proceeds helps give a child a bed of their own',
    logo:'',
    link:'',
    ariaLabel:'',
  }
</script>

<div id="CLP-Main">
  <Hero content={hero}/>
  <ShopBy catagories={shopby} />
  <Marquee marquees={marquees}/>
  <Corporate corporate={corporate}/>
  <Ad ad={ad} />
</div>
