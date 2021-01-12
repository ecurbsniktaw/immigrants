<!-- 
    BODY.SVELTE
    This is the main body of the Immigrant Ancestors page.
    For each family in the families object, one Family component is displayed.
 -->

{#each families as family}
    <div>
        <Family 
            famText={family.famText} 
            names={family.famName} 
            people={family.people} 
            couple={family.couple}
        />
    </div>
{/each}

<style>

</style>

<script>
    import Family from './Family.svelte';

	let families = [
		{
            id: 1,
            famText: 'Bruce’s great great grandfather Louis Poullain (later Ballard) was born in France, emigrated to Western New York at age 23, and died in Langford, NY in 1887 at age 77.',
            couple: 
            {
                theirNames: 'Louis and Mary Ballard',
                theirRelationship: "Delores Kirsch Watkins' Maternal Great Grandparents"
            },
            people: [
                {
                    personName: 'Louis Ballard',
                    personBorn: '7 May 1810, France',
                    personArv: '29 Oct 1833, 23 years old',
                    personDied: '12 Dec 1887, Langford, NY, 77',
                    personPic: 'https://brucewatkins.org/ancestry/images/withTrowel.crop.jpg'
                },
                {
                    personName: 'Mary Daul Ballard',
                    personBorn: 'about 1816, France',
                    personArv: 'before 1836',
                    personDied: '22 Nov 1886, Langford, 70',
                    personPic: 'https://brucewatkins.org/ancestry/images/maryDole100.jpg'
                }
            ]
		},
		{
			id: 2,
            famText: 'about the Bohns',
            couple: 
            {
                theirNames: 'Jacob and Mary Bohn',
                theirRelationship: "Delores Kirsch Watkins' Maternal Great Grandparents"
            },
            people: [
                {
                    personName: 'Jacob J Bohn',
                    personBorn: '2 Jan 1813, France',
                    personArv: '22 Oct 1847, 34 years old',
                    personDied: '20 Jan 1875, Sheldon, NY, 62',
                    personPic: 'https://brucewatkins.org/ancestry/images/profileM.jpg'
                },
                {
                    personName: 'Mary Voss Armbrust Bohn',
                    personBorn: '12 Nov 1823, France',
                    personArv: '15 Nov 1853, 30 years old',
                    personDied: '27 Sep 1915, Buffalo, NY, 91',
                    personPic: 'https://brucewatkins.org/ancestry/images/1900.bohn.maryann.jpg'
                }
            ]
		},
		{
			id: 3,
            famName: "Peter and  Katherine Kirsch<br> Paternal Grandparents of Delores Kirsch Watkins",
            famText: 'about the Kirsch family',
            couple: 
            {
                theirNames: 'Peter and Katherine Kirsch',
                theirRelationship: "Delores Kirsch Watkins' Paternal Grandparents"
            },
            people: [
                {
                    personName: 'Peter Kirsch',
                    personBorn: '20 Dec 1852, France',
                    personArv: '13 May 1872, age 19',
                    personDied: '23 Aug 1919, Buffalo, NY, 66',
                    personPic: 'https://brucewatkins.org/ancestry/images/peterKthumb.jpg'
                },
                {
                    personName: 'Katherine Koop Kirsch',
                    personBorn: '1 May 1849, France',
                    personArv: '1872, age 23',
                    personDied: '9 May 1913, Buffalo, NY, 64',
                    personPic: 'https://brucewatkins.org/ancestry/images/kKirsch.jpg'
                }
            ]
		},
		{
			id: 4,
            famName: "The Watkin's: Paternal Grandparents and Father of Bruce Watkins",
            famText: 'about the Watkin(s) family',
            couple: 
            {
                theirNames: 'William, Martha and Robert Watkin',
                theirRelationship: "Bruce Watkins' Paternal Grandparents and Father"
            },
            people: [
                {
                    personName: 'William Watkin',
                    personBorn: '24 Dec 1888, England',
                    personArv: '15 Feb 1922, 33 years old',
                    personDied: '19 Sep 1964 (75), Canton, Ohio',
                    personPic: 'http://brucewatkins.org/ancestry/images/wmWatkin.sq.jpg'
                },
                {
                    personName: 'Martha Warburton Watkin',
                    personBorn: '2 Feb 1891, Enland',
                    personArv: '15 Feb 1922, 31 years old',
                    personDied: '3 Jun 1970 (79), Buffalo, NY',
                    personPic: 'http://brucewatkins.org/ancestry/images/marthaW.jpg'
                },
                {
                    personName: 'Robert R Watkins',
                    personBorn: '3 Sep 1912',
                    personArv: '15 Feb 1922, 9 years old',
                    personDied: '25 Nov 1969, Buffalo, NY, 57',
                    personPic: 'https://brucewatkins.org/ancestry/images/rrWatkinsHS100.jpg'
                }
            ]
		},
		{
			id: 5,
            famName: "The Ginsbergs: Maternal Grandparents of Stanley Solow",
            famText: 'about the Ginsberg family',
            couple: 
            {
                theirNames: 'Samuel and Rose Ginsberg',
                theirRelationship: "Stanley Solow's Maternal Grandparents"
            },
            people: [
                {
                    personName: 'Samuel Ginsberg',
                    personBorn: '15 Oct 1870',
                    personArv: 'sometime',
                    personDied: 'unknown',
                    personPic: 'https://brucewatkins.org/ancestry/images/samuelGinsberg100.jpg'
                },
                {
                    personName: 'Rose Wilensky Ginsberg',
                    personBorn: '1867',
                    personArv: 'sometime',
                    personDied: '15 Dec 1933 (66)',
                    personPic: 'https://brucewatkins.org/ancestry/images/profileF.jpg'
                }
            ]
		},
		{
			id: 6,
            famName: "Joseph Solow: Stanley Solow's Father",
            famText: 'about the Solow family',
            couple: 
            {
                theirNames: 'Joseph Solow',
                theirRelationship: "Stanley Solow's Father"
            },
            people: [
                {
                    personName: 'Joseph Solow',
                    personBorn: '10 Apr 1889',
                    personArv: 'sometime',
                    personDied: '3 May 1956 (67)',
                    personPic: 'http://brucewatkins.org/ancestry/images/familyJoeSolowThumb.jpg'
                }
            ]
		},
		{
			id: 7,
            famName: "The Borensteins: Freda Borenstein Solow's Parents",
            famText: 'about the Borenstein family',
            couple: 
            {
                theirNames: 'Sidney and Rose Borenstein',
                theirRelationship: "Freda Borenstein Solow's Parents"
            },
            people: [
                {
                    personName: 'Sidney Borenstein',
                    personBorn: '1894',
                    personArv: 'sometime',
                    personDied: '3 Mar 1986 (92)',
                    personPic: 'http://brucewatkins.org/ancestry/images/sBorenstein.jpg'
                },
                {
                    personName: 'Rose Gottlieb Borenstein',
                    personBorn: '5 Feb 1898',
                    personArv: 'sometime',
                    personDied: '5 Dec 1968 (70)',
                    personPic: 'http://brucewatkins.org/ancestry/images/rBorenstein.jpg'
                }
            ]
		},
    ]
    
</script>
