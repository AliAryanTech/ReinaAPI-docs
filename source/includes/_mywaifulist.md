# MyWaifuList

## Random

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/random`

### Query Parameters
Parameter | Required | Description
--------- | -------- | -----------
type        | false     | Type of the character (waifu/husbando)

> The response schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "name": "Rito Sudou",
        "gender": "Female",
        "likes": {
            "count": 9,
            "rank": 22608
        },
        "trash": {
            "count": 3,
            "rank": 18460
        },
        "image": "https://thicc.mywaifulist.moe/waifus/6865/26579d094b7569696a46e14802608e4b65af340c7150bd1ef2866524ff6c7fa6_thumb.jpeg",
        "slug": "rito-sudou",
        "nsfw": false,
        "tags": [],
        "is_vtuber": false,
        "original_name": "須藤 りと",
        "romaji_name": null,
        "appearances": [
            {
                "name": "Urahara",
                "slug": "urahara",
                "image": null,
                "description": "",
                "url": "https://mywaifulist.moe/waifu/urahara"
            }
        ],
        "origin": null,
        "age": null,
        "birthday": null,
        "height": null,
        "weight": null,
        "blood_type": null,
        "bust": null,
        "waist": null,
        "hip": null,
        "popularity_rank": 22779,
        "description": "No biography written.",
        "url": "https://mywaifulist.moe/waifu/rito-sudou"
    }
}
```

This endpoint gets a random Waifu/Husbando from MyWaifuList and returns the information of the character.

## Get Character Details By Slug

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/character/:slug`

### Path Parameters
Parameter | Required | Description
--------- | -------- | -----------
slug     | true     | Slug of the character from MyWaifuList

> The response schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "name": "Kirisaki Chitoge",
        "gender": "Female",
        "likes": {
            "count": 1987,
            "rank": 103
        },
        "trash": {
            "count": 640,
            "rank": 61
        },
        "image": "https://thicc.mywaifulist.moe/waifus/132/b5aae2947b7f7419d9f332f07a275db6784d9100bd003fc2a4fd4f382790c7b4_thumb.png",
        "slug": "kirisaki-chitoge",
        "nsfw": false,
        "tags": [
            "blonde hair"
        ],
        "is_vtuber": false,
        "original_name": "桐崎 千棘, Ichijō Chitoge",
        "romaji_name": null,
        "appearances": [
            {
                "name": "Nisekoi: False Love",
                "slug": "nisekoi-false-love",
                "image": "https://thicc.mywaifulist.moe/series/94/4deb14f4a2ab2b7f04a95db39f8ba2c2a2d5a20ba73988c79f1c0195ccd0066c_thumbnail.jpeg",
                "description": "Raku Ichijou, a first-year student at Bonyari High School, is the sole heir to an intimidating yakuza family. Ten years ago, Raku made a promise to his childhood friend. Now, all he has to go on is a pendant with a lock, which can only be unlocked with the key which the girl took with her when they parted.\r\n\r\nNow, years later, Raku has grown into a typical teenager, and all he wants is to remain as uninvolved in his yakuza background as possible while spending his school days alongside his middle school crush Kosaki Onodera. However, when the American Bee Hive Gang invades his family's turf, Raku's idyllic romantic dreams are sent for a toss as he is dragged into a frustrating conflict: Raku is to pretend that he is in a romantic relationship with Chitoge Kirisaki, the beautiful daughter of the Bee Hive's chief, so as to reduce the friction between the two groups. Unfortunately, reality could not be farther from this whopping lie—Raku and Chitoge fall in hate at first sight, as the girl is convinced he is a pathetic pushover, and in Raku's eyes, Chitoge is about as attractive as a savage gorilla. \r\n\r\nNisekoi follows the daily antics of this mismatched couple who have been forced to get along for the sake of maintaining the city's peace. With many more girls popping up his life, all involved with Raku's past somehow, his search for the girl who holds his heart and his promise leads him in more unexpected directions than he expects.\r\n\r\n[Written by MAL Rewrite]",
                "url": "https://mywaifulist.moe/series/nisekoi-false-love"
            }
        ],
        "origin": "America",
        "age": null,
        "birthday": "June 7th",
        "height": "160.00 cm",
        "weight": "46.00 kg",
        "blood_type": "B",
        "bust": null,
        "waist": null,
        "hip": null,
        "popularity_rank": 78,
        "description": "Chitoge Kirisaki originally lived with her father in the United States until she transferred to another school in Japan — where she is now currently residing in. With her father being the leader of the infamous Bee Hive Gang, it has effectively caused multiple problems for Chitoge during her childhood as she was unable to make friends very easily due to being under constant watch by her bodyguard, Claude. However, when she was young, she met and befriended a hitwoman in-training, Tsugumi, who, to the current day, she is still friends with. Chitoge also seems to have a few problems with her mother, who has very high expectations for her, making Chitoge somewhat of a perfectionist who excels in both sports and academics.\n\nAt some point during her childhood, Chitoge had become close friends with Raku, Kosaki, Marika, and Yui through a summer vacation in Tegu Plateau. Chitoge and Kosaki had the strongest relationship between the whole group and both shared a love for a picture book Chitoge owned which was about a princess and prince falling in love and reuniting in heaven. Chitoge decided to give Kosaki the picture book as a sign of friendship and remembrance when they can longer see each other.",
        "url": "https://mywaifulist.moe/waifu/kirisaki-chitoge"
    }
}
```

This endpoint returns the character's information of the given character's slug from MyWaifuList.

## Character Search by Name

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/character`

### Query Parameters
Parameter | Required | Description
--------- | -------- | -----------
q        | false     | Name of the character to search
page     | false     | Page of the character search
type     | false     | Type of the character (all/husbando)

> The response schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "pagination": {
        "current_page": 1,
        "total_pages": 1,
        "has_next_page": false
    },
    "data": [
        {
            "name": "Reina Izumi",
            "slug": "reina-izumi",
            "original_name": "和泉 玲奈",
            "appearances": [
                {
                    "name": "Myriad Colors Phantom World",
                    "original_name": "無彩限のファントム・ワールド",
                    "slug": "myriad-colors-phantom-world",
                    "url": "https://mywaifulist.moe/series/myriad-colors-phantom-world"
                }
            ],
            "image": "https://thicc.mywaifulist.moe/waifus/1232/6bd02a8775a3c1fe7632fc15545fab102af034df9a33d23e6d4fd58d15b28911_thumb.jpg",
            "url": "https://mywaifulist.moe/waifu/reina-izumi"
        }
    ]
}
```

This endpoint searches for a character by its name from MyWaifuList.

## Get Waifu of the day

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/waifu-of-the-day`

> The response schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "name": "Charlotte",
        "gender": "Female",
        "likes": {
            "count": 138,
            "rank": 3713
        },
        "trash": {
            "count": 10,
            "rank": 8004
        },
        "image": "https://thicc.mywaifulist.moe/waifus/30250/c98c9d19ee63a671c5346d974934bd1dbf968485d5e8d29f0d273174da064b86_thumb.jpeg",
        "slug": "charlotte-7",
        "nsfw": false,
        "tags": [],
        "is_vtuber": false,
        "original_name": "シャーロット",
        "romaji_name": "Charlotte",
        "appearances": [
            {
                "name": "Fly Me to the Moon (Manga)",
                "slug": "fly-me-to-the-moon-manga",
                "image": "https://thicc.mywaifulist.moe/series/3804/b15840735762aa56a0b4716089105e0632ef7e66d8662c04ce4c263c7f969b27_thumbnail.jpeg",
                "description": "Having grown up ridiculed for his bizarre name, Nasa Yuzaki strives to be remembered for something more. Fortunately, it seems he's on the right path, ranking first in the nation's mock exams and set to enter his high school of choice.\r\n\r\nHowever, everything changes in a single night when he notices a girl across the street on his way home. Enraptured by her overwhelming cuteness, it's love at first sight for Nasa. But in his infatuated daze, he fails to notice the approaching danger speeding down the road and finds himself at death's door. Barely alive thanks to the girl's intervention, Nasa musters the courage to confess his love to her, fearing she might otherwise vanish from his life. She accepts his proposal on one condition: marriage, to which Nasa gladly accepts before passing out from his injuries. Upon waking, however, the girl is nowhere to be found.\r\n\r\nAfter recovering from his injuries, Nasa tosses his previous ambitions aside and dedicates his life to finding the girl that captured his heart, yet several years pass to no avail. But one night, when an unexpected visitor comes knocking on his door, Nasa finds himself facing a woman that would forever change his world: his wife.",
                "url": "https://mywaifulist.moe/series/fly-me-to-the-moon-manga"
            },
            {
                "name": "Fly Me to the Moon",
                "slug": "fly-me-to-the-moon",
                "image": "https://thicc.mywaifulist.moe/series/5229/b40d16cc1cffb4564a4798d4861d02fb2a22ceac0c62653fda7cd48e229e46f9_thumbnail.jpeg",
                "description": "Having grown up ridiculed for his bizarre name, Nasa Yuzaki strives to be remembered for something more. Fortunately, it seems he's on the right path, ranking first in the nation's mock exams and set to enter his high school of choice.\r\n\r\nHowever, everything changes in a single night when he notices a girl across the street on his way home. Enraptured by her overwhelming cuteness, it's love at first sight for Nasa. But in his infatuated daze, he fails to notice the approaching danger speeding down the road and finds himself at death's door. Barely alive thanks to the girl's intervention, Nasa musters the courage to confess his love to her, fearing she might otherwise vanish from his life. She accepts his proposal on one condition: marriage, to which Nasa gladly accepts before passing out from his injuries. Upon waking, however, the girl is nowhere to be found.\r\n\r\nAfter recovering from his injuries, Nasa tosses his previous ambitions aside and dedicates his life to finding the girl that captured his heart, yet several years pass to no avail. But one night, when an unexpected visitor comes knocking on his door, Nasa finds himself facing a woman that would forever change his world: his wife.",
                "url": "https://mywaifulist.moe/series/fly-me-to-the-moon"
            }
        ],
        "origin": null,
        "age": null,
        "birthday": null,
        "height": null,
        "weight": null,
        "blood_type": null,
        "bust": null,
        "waist": null,
        "hip": null,
        "popularity_rank": 4155,
        "description": "She always wears her maid outfit while at work and has very long wavy hair.",
        "url": "https://mywaifulist.moe/waifu/charlotte-7"
    }
}
```

This endpoint returns the data for waifu of the day in MyWaifuList.

## Get Popular Waifus

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/popular`

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Most Popular Anime Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Megumin",
                    "original_name": "めぐみん",
                    "slug": "megumin-konosuba-god-s-blessing-on-this-wonderful-world",
                    "image": "https://thicc.mywaifulist.moe/waifus/319/2b9e5c31ae2168b769d64350f07526363208d7e2ca2d6b11bf4ca7bba8de9dc6_thumb.png",
                    "popularity_rank": 1,
                    "like_rank": 1,
                    "trash_rank": 4,
                    "url": "https://mywaifulist.moe/waifu/megumin-konosuba-god-s-blessing-on-this-wonderful-world"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Rem",
                    "original_name": "レム",
                    "slug": "rem-re-zero-starting-life-in-another-world",
                    "image": "https://thicc.mywaifulist.moe/waifus/41/5d01a3827544918e005287f16d1e7132d0b873dbb628a9d565449745c0ed60c1_thumb.jpg",
                    "popularity_rank": 2,
                    "like_rank": 2,
                    "trash_rank": 6,
                    "url": "https://mywaifulist.moe/waifu/rem-re-zero-starting-life-in-another-world"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Asuna Yuuki",
                    "original_name": "結城 明日奈",
                    "slug": "asuna-yuuki-sword-art-online",
                    "image": "https://thicc.mywaifulist.moe/waifus/58/c73fb4b96627b9ba3b52cc3ae051fd10e0efe87c30c026473ae9936220e6949c_thumb.jpg",
                    "popularity_rank": 3,
                    "like_rank": 14,
                    "trash_rank": 1,
                    "url": "https://mywaifulist.moe/waifu/asuna-yuuki-sword-art-online"
                }
            },
            {
                "rank": 4,
                "waifu": {
                    "name": "Zero Two",
                    "original_name": "ゼロツー",
                    "slug": "zero-two-darling-in-the-franxx",
                    "image": "https://thicc.mywaifulist.moe/waifus/9215/7e6b971558af535d52397df6854c3c90bb66a41c5faaa07395d0a65e4e20fead_thumb.jpeg",
                    "popularity_rank": 4,
                    "like_rank": 4,
                    "trash_rank": 13,
                    "url": "https://mywaifulist.moe/waifu/zero-two-darling-in-the-franxx"
                }
            },
            {
                "rank": 47,
                "waifu": {
                    "name": "Historia Reiss",
                    "original_name": "ヒストリア・レイス",
                    "slug": "historia-reiss-attack-on-titan",
                    "image": "https://thicc.mywaifulist.moe/waifus/2950/aabd70daa845cc70a9ee26eff355cd7a12be34ca727a51b8ea924421bd3f31f1_thumb.png",
                    "popularity_rank": 47,
                    "like_rank": 44,
                    "trash_rank": 86,
                    "url": "https://mywaifulist.moe/waifu/historia-reiss-attack-on-titan"
                }
            },
            {
                "rank": 48,
                "waifu": {
                    "name": "Wiz",
                    "original_name": "ウィズ",
                    "slug": "wiz",
                    "image": "https://thicc.mywaifulist.moe/waifus/1804/73dfaee92b1f25d94c32829dc7bb37f782b2d4e2b21afba9a511f9dad13f3726_thumb.jpg",
                    "popularity_rank": 48,
                    "like_rank": 42,
                    "trash_rank": 131,
                    "url": "https://mywaifulist.moe/waifu/wiz"
                }
            },
            {
                "rank": 49,
                "waifu": {
                    "name": "Tamamo-no-Mae",
                    "original_name": "玉藻の前",
                    "slug": "tamamo-no-mae-fate-extra",
                    "image": "https://thicc.mywaifulist.moe/waifus/685/584e6c3b17d316cec3b9ada0ab27d9eed4a3baaec8af09bdeb119502269878d4_thumb.jpeg",
                    "popularity_rank": 49,
                    "like_rank": 49,
                    "trash_rank": 68,
                    "url": "https://mywaifulist.moe/waifu/tamamo-no-mae-fate-extra"
                }
            },
            {
                "rank": 50,
                "waifu": {
                    "name": "Shino Asada",
                    "original_name": "朝田 詩乃",
                    "slug": "shino-asada-sword-art-online",
                    "image": "https://thicc.mywaifulist.moe/waifus/528/464a10e4e9e446df154b19185055c404c494caf825ec398c3bf9bc95297199c9_thumb.jpg",
                    "popularity_rank": 50,
                    "like_rank": 46,
                    "trash_rank": 87,
                    "url": "https://mywaifulist.moe/waifu/shino-asada-sword-art-online"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the most popular waifus of all time in MyWaifuList.

## Get Best Waifus

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/best`

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Best Anime Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Mizore Shirayuki",
                    "original_name": "白雪 みぞれ",
                    "slug": "mizore-shirayuki-rosario-vampire",
                    "image": "https://thicc.mywaifulist.moe/waifus/720/09eea57d6ecd06353aa75e6689a7da955ac183e5d5e26d314e2e742492b0e13b_thumb.jpg",
                    "popularity_rank": 419,
                    "like_rank": 363,
                    "trash_rank": 1587,
                    "url": "https://mywaifulist.moe/waifu/mizore-shirayuki-rosario-vampire"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Dr. Franken Stein",
                    "original_name": "フランケン•シュタイン",
                    "slug": "dr-franken-stein",
                    "image": "https://thicc.mywaifulist.moe/waifus/23998/fd3a43f719a3b39f5fb0273c8b98d0c6eb446d32a869e118a5d3fa51395ded0c_thumb.jpg",
                    "popularity_rank": 5154,
                    "like_rank": 4402,
                    "trash_rank": 16648,
                    "url": "https://mywaifulist.moe/waifu/dr-franken-stein"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Rit",
                    "original_name": "リット",
                    "slug": "rit-banished-from-the-hero-s-party-i-decided-to-live-a-quiet-life-in-the-countryside",
                    "image": "https://thicc.mywaifulist.moe/waifus/29717/358ea2d48e8b689353fe38d7913aee0c68cb4fcd5b57def1c3e0831edafdcb97_thumb.jpeg",
                    "popularity_rank": 3276,
                    "like_rank": 2821,
                    "trash_rank": 10124,
                    "url": "https://mywaifulist.moe/waifu/rit-banished-from-the-hero-s-party-i-decided-to-live-a-quiet-life-in-the-countryside"
                }
            },
            {
                "rank": 4,
                "waifu": {
                    "name": "Miko Yotsuya",
                    "original_name": "四谷みこ",
                    "slug": "miko-yotsuya-mieruko-chan",
                    "image": "https://thicc.mywaifulist.moe/waifus/37299/2a6a7ace7e7a1e962e587a3102d6ce667b95dd336960aab51b76f9d11f62298a_thumb.jpg",
                    "popularity_rank": 615,
                    "like_rank": 535,
                    "trash_rank": 2293,
                    "url": "https://mywaifulist.moe/waifu/miko-yotsuya-mieruko-chan"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the best waifus of all time in MyWaifuList.

## Get Popular V-Tubers

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/vtubers`

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Most Popular Virtual Youtubers",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "AI Kizuna",
                    "original_name": "キズナアイ",
                    "slug": "kizuna-ai-youtube",
                    "image": "https://thicc.mywaifulist.moe/waifus/1608/0cfc122410eeb4182bcc67aea3f8074e017147f855559edfc6bc6f119d39cd45_thumb.jpg",
                    "popularity_rank": 189,
                    "like_rank": 166,
                    "trash_rank": 358,
                    "url": "https://mywaifulist.moe/waifu/kizuna-ai-youtube"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Gura Gawr",
                    "original_name": "がうる・ぐら",
                    "slug": "gura-gawr-hololive-production",
                    "image": "https://thicc.mywaifulist.moe/waifus/32382/ff8853b7432256707ee547591a8c9023285ec9224048d1275273d87615666203_thumb.jpg",
                    "popularity_rank": 219,
                    "like_rank": 224,
                    "trash_rank": 273,
                    "url": "https://mywaifulist.moe/waifu/gura-gawr-hololive-production"
                }
            },
            {
                "rank": 17,
                "waifu": {
                    "name": "Subaru Oozora",
                    "original_name": "大空スバル",
                    "slug": "subaru-oozora-hololive-production",
                    "image": "https://thicc.mywaifulist.moe/waifus/28462/4ecf9001d7a0d04f1f5e222655fce6bbbd7b076cd8e92fd1d17d7e0d8cb60344_thumb.jpg",
                    "popularity_rank": 811,
                    "like_rank": 695,
                    "trash_rank": 2669,
                    "url": "https://mywaifulist.moe/waifu/subaru-oozora-hololive-production"
                }
            },
            {
                "rank": 18,
                "waifu": {
                    "name": "Towa Tokoyami",
                    "original_name": "常闇トワ",
                    "slug": "towa-tokoyami-hololive-production",
                    "image": "https://thicc.mywaifulist.moe/waifus/29235/3dd4aee02988ac4e2fa648b34556ddf7c7f192507e7d5bda4e7ca333207915e6_thumb.jpg",
                    "popularity_rank": 894,
                    "like_rank": 774,
                    "trash_rank": 3061,
                    "url": "https://mywaifulist.moe/waifu/towa-tokoyami-hololive-production"
                }
            },
            {
                "rank": 19,
                "waifu": {
                    "name": "Mio Ookami",
                    "original_name": "大神ミオ",
                    "slug": "mio-ookami-azur-lane",
                    "image": "https://thicc.mywaifulist.moe/waifus/25062/d405aad29c40629ef950b96779128c92f27aac89cd3b810a216f95b62ec872ac_thumb.png",
                    "popularity_rank": 925,
                    "like_rank": 803,
                    "trash_rank": 3165,
                    "url": "https://mywaifulist.moe/waifu/mio-ookami-azur-lane"
                }
            },
            {
                "rank": 20,
                "waifu": {
                    "name": "Miko Sakura",
                    "original_name": "さくらみこ",
                    "slug": "miko-sakura-hololive-production",
                    "image": "https://thicc.mywaifulist.moe/waifus/30238/5f8e8156d90a79ed01e2181353db359cf6bea5a46a6fbfdaadf3450a9f4e3ff3_thumb.png",
                    "popularity_rank": 945,
                    "like_rank": 823,
                    "trash_rank": 2981,
                    "url": "https://mywaifulist.moe/waifu/miko-sakura-hololive-production"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the most popular v-tubers of all time in MyWaifuList.

## Get Trash Waifus

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/trash`

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Worst Anime Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Malty S Melromarc",
                    "original_name": "マルティ＝S＝メルロマルク",
                    "slug": "malty-melromarc-the-rising-of-the-shield-hero",
                    "image": "https://thicc.mywaifulist.moe/waifus/2090/e94dd823bf4895d1f788739261ef40bdf62e0b6ec6c1ac35a66a8eb5c5175926_thumb.jpeg",
                    "popularity_rank": 23,
                    "like_rank": 1476,
                    "trash_rank": 2,
                    "url": "https://mywaifulist.moe/waifu/malty-melromarc-the-rising-of-the-shield-hero"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Akemi Hinazuki",
                    "original_name": "雛月明美",
                    "slug": "akemi-hinazuki",
                    "image": "https://thicc.mywaifulist.moe/waifus/3907/b6a3d87181ef185a390b96e5fe541513a5b6d86e5d3a8e257743f8d623c3f6c7_thumb.jpeg",
                    "popularity_rank": 62,
                    "like_rank": 6769,
                    "trash_rank": 3,
                    "url": "https://mywaifulist.moe/waifu/akemi-hinazuki"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Nobuyuki Sugou",
                    "original_name": "須郷伸之",
                    "slug": "nobuyuki-sugou-sword-art-online",
                    "image": "https://thicc.mywaifulist.moe/waifus/6102/fe5056fa3f431b73be1b9bfd203e3b725c8b988f534dff09aaaaa6d7cc769939_thumb.jpeg",
                    "popularity_rank": 114,
                    "like_rank": 7197,
                    "trash_rank": 9,
                    "url": "https://mywaifulist.moe/waifu/nobuyuki-sugou-sword-art-online"
                }
            },
            {
                "rank": 4,
                "waifu": {
                    "name": "Motoyasu Kitamura",
                    "original_name": "北村元康",
                    "slug": "motoyasu-kitamura-the-rising-of-the-shield-hero",
                    "image": "https://thicc.mywaifulist.moe/waifus/21066/4bd15973c397efb0dfea4d52d933475ac324a1f9507a8af168b788ba4dc85032_thumb.jpeg",
                    "popularity_rank": 137,
                    "like_rank": 6586,
                    "trash_rank": 10,
                    "url": "https://mywaifulist.moe/waifu/motoyasu-kitamura-the-rising-of-the-shield-hero"
                }
            },
            {
                "rank": 5,
                "waifu": {
                    "name": "Shinji Matou",
                    "original_name": "間桐 慎二",
                    "slug": "shinji-matou-fate-stay-night",
                    "image": "https://thicc.mywaifulist.moe/waifus/6104/087b8ce0b1d8c5c0d83912d4b868e67e37fb6ccc673697d80f4eee1faf4f7169_thumb.jpeg",
                    "popularity_rank": 141,
                    "like_rank": 5407,
                    "trash_rank": 11,
                    "url": "https://mywaifulist.moe/waifu/shinji-matou-fate-stay-night"
                }
            },
            {
                "rank": 49,
                "waifu": {
                    "name": "Public Safety Commission President",
                    "original_name": "公安委員会会長",
                    "slug": "public-safety-commission-president",
                    "image": "https://thicc.mywaifulist.moe/waifus/19503/cd53af713e8c7fd7ccf79fddb03cca49dde14c965c0a2a0fdfcf4ccde54f5633_thumb.png",
                    "popularity_rank": 5319,
                    "like_rank": 25949,
                    "trash_rank": 810,
                    "url": "https://mywaifulist.moe/waifu/public-safety-commission-president"
                }
            },
            {
                "rank": 50,
                "waifu": {
                    "name": "Kamado Ueshita",
                    "original_name": "上下 かまど",
                    "slug": "kamado-ueshita",
                    "image": "https://thicc.mywaifulist.moe/waifus/22664/68bf3f51332ddba18212710a1243d873c3f454a66d6b1ee045da5d7770f6090a_thumb.png",
                    "popularity_rank": 5279,
                    "like_rank": 22984,
                    "trash_rank": 830,
                    "url": "https://mywaifulist.moe/waifu/kamado-ueshita"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the worst waifus of all time in MyWaifuList.

## Get Popular Waifus for the current Season

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/current/popular`

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Summer 2022 Most Popular Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Albedo",
                    "original_name": "アルベド",
                    "slug": "albedo-overlord",
                    "image": "https://thicc.mywaifulist.moe/waifus/651/805deb0689c2b3e850e8e9e851694b36ac2a98f6d7b78b6299182181ade157a3_thumb.jpg",
                    "popularity_rank": 39,
                    "like_rank": 38,
                    "trash_rank": 122,
                    "url": "https://mywaifulist.moe/waifu/albedo-overlord"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Hestia",
                    "original_name": "ヘスティア",
                    "slug": "hestia-is-it-wrong-to-try-to-pick-up-girls-in-a-dungeon",
                    "image": "https://thicc.mywaifulist.moe/waifus/794/dbb11133b0183184cb32f528bf4ea3d1d0cb5ca75f78fd8d18addb9aac0af359_thumb.png",
                    "popularity_rank": 58,
                    "like_rank": 57,
                    "trash_rank": 155,
                    "url": "https://mywaifulist.moe/waifu/hestia-is-it-wrong-to-try-to-pick-up-girls-in-a-dungeon"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Chizuru Ichinose",
                    "original_name": "一ノ瀬 千鶴",
                    "slug": "chizuru-ichinose-rent-a-girlfriend",
                    "image": "https://thicc.mywaifulist.moe/waifus/13496/5896d38e5b89cb3b8d5de733dfbd6a8b7ed59d835621f22f7f9a50ee62294285_thumb.jpeg",
                    "popularity_rank": 84,
                    "like_rank": 73,
                    "trash_rank": 286,
                    "url": "https://mywaifulist.moe/waifu/chizuru-ichinose-rent-a-girlfriend"
                }
            },
            {
                "rank": 14,
                "waifu": {
                    "name": "Suzune Horikita",
                    "original_name": "堀北 鈴音",
                    "slug": "suzune-horikita-classroom-of-the-elite",
                    "image": "https://thicc.mywaifulist.moe/waifus/6297/0778d0589411a5d553cd17d9b2bc0cfe951e670024b7399f4daea3a6cbc42aab_thumb.png",
                    "popularity_rank": 358,
                    "like_rank": 323,
                    "trash_rank": 1135,
                    "url": "https://mywaifulist.moe/waifu/suzune-horikita-classroom-of-the-elite"
                }
            },
            {
                "rank": 15,
                "waifu": {
                    "name": "Mary Saotome",
                    "original_name": "早乙女 芽亜里",
                    "slug": "mary-saotome-kakegurui-compulsive-gambler",
                    "image": "https://thicc.mywaifulist.moe/waifus/6168/1fe3077110d9840524eaf2e50f48253c4fd394a7fafe4fb686ff8fa115b7a32c_thumb.jpg",
                    "popularity_rank": 368,
                    "like_rank": 333,
                    "trash_rank": 910,
                    "url": "https://mywaifulist.moe/waifu/mary-saotome-kakegurui-compulsive-gambler"
                }
            }
        ]
    }
}
```

This endpoint returns the most popular waifus for the current season in MyWaifuList.

## Get Best Waifus for the current Season

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/current/best`

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Summer 2022 Best Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Chizuru Ichinose",
                    "original_name": "一ノ瀬 千鶴",
                    "slug": "chizuru-ichinose-rent-a-girlfriend",
                    "image": "https://thicc.mywaifulist.moe/waifus/13496/5896d38e5b89cb3b8d5de733dfbd6a8b7ed59d835621f22f7f9a50ee62294285_thumb.jpeg",
                    "popularity_rank": 84,
                    "like_rank": 73,
                    "trash_rank": 286,
                    "url": "https://mywaifulist.moe/waifu/chizuru-ichinose-rent-a-girlfriend"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Evileye",
                    "original_name": "イビルアイ",
                    "slug": "evileye-overlord",
                    "image": "https://thicc.mywaifulist.moe/waifus/8967/75dbc4ac7652e778c7d462e6b04ca0072da0e693a5719bb923c274280e717d2b_thumb.png",
                    "popularity_rank": 697,
                    "like_rank": 612,
                    "trash_rank": 1787,
                    "url": "https://mywaifulist.moe/waifu/evileye-overlord"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Arisu Sakayanagi",
                    "original_name": "坂柳 有栖",
                    "slug": "arisu-sakayanagi-classroom-of-the-elite",
                    "image": "https://thicc.mywaifulist.moe/waifus/10726/4fbee3e2c3d1ddccc143d0dad752a22f2215af9176d37af073283e9f580f8eaa_thumb.jpg",
                    "popularity_rank": 1683,
                    "like_rank": 1500,
                    "trash_rank": 4244,
                    "url": "https://mywaifulist.moe/waifu/arisu-sakayanagi-classroom-of-the-elite"
                }
            },
            {
                "rank": 19,
                "waifu": {
                    "name": "Honami Ichinose",
                    "original_name": "一之瀬 帆波",
                    "slug": "honami-ichinose-classroom-of-the-elite",
                    "image": "https://thicc.mywaifulist.moe/waifus/7838/225705d66045525ff784b2649a3fffad6dfaf8537d224707607ef1d9354f1456_thumb.jpg",
                    "popularity_rank": 595,
                    "like_rank": 505,
                    "trash_rank": 2292,
                    "url": "https://mywaifulist.moe/waifu/honami-ichinose-classroom-of-the-elite"
                }
            },
            {
                "rank": 20,
                "waifu": {
                    "name": "Lilith",
                    "original_name": "",
                    "slug": "lilith-my-recently-hired-maid-is-suspicious",
                    "image": "https://thicc.mywaifulist.moe/waifus/28232/63a2d4cc5e99010932e2b80f9e1e458e75d330d2604aac0d55353d851af12845_thumb.png",
                    "popularity_rank": 7408,
                    "like_rank": 6322,
                    "trash_rank": 23120,
                    "url": "https://mywaifulist.moe/waifu/lilith-my-recently-hired-maid-is-suspicious"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the best waifus for the current season in MyWaifuList.

## Get Trash Waifus for the current Season

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/current/trash`

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Summer 2022 Worst Waifus",
        "data": [
            {
                "rank": 1,
                "waifu": {
                    "name": "Mami Nanami",
                    "original_name": "七海麻美",
                    "slug": "mami-nanami-rent-a-girlfriend",
                    "image": "https://thicc.mywaifulist.moe/waifus/27411/b9496a6944b1ef43b6ee700486fbf8cdaf02242ea15a4620c7606d8fe988eec9_thumb.jpeg",
                    "popularity_rank": 234,
                    "like_rank": 1002,
                    "trash_rank": 34,
                    "url": "https://mywaifulist.moe/waifu/mami-nanami-rent-a-girlfriend"
                }
            },
            {
                "rank": 2,
                "waifu": {
                    "name": "Kazuya Kinoshita",
                    "original_name": "木ノ下 和也",
                    "slug": "kazuya-kinoshita-rent-a-girlfriend",
                    "image": "https://thicc.mywaifulist.moe/waifus/27410/7176096a2040be5459258871aae093ae4ede73c773735211620185bb2c66bfa8_thumb.jpeg",
                    "popularity_rank": 1143,
                    "like_rank": 6747,
                    "trash_rank": 99,
                    "url": "https://mywaifulist.moe/waifu/kazuya-kinoshita-rent-a-girlfriend"
                }
            },
            {
                "rank": 3,
                "waifu": {
                    "name": "Apollo",
                    "original_name": "アポロン",
                    "slug": "apollo-is-it-wrong-to-try-to-pick-up-girls-in-a-dungeon",
                    "image": "https://thicc.mywaifulist.moe/waifus/23094/fbcf881affc384ded4d0640a05fc589b32a5889dce49b9a20f19ebed5cfbed6a_thumb.png",
                    "popularity_rank": 1349,
                    "like_rank": 15792,
                    "trash_rank": 112,
                    "url": "https://mywaifulist.moe/waifu/apollo-is-it-wrong-to-try-to-pick-up-girls-in-a-dungeon"
                }
            },
            {
                "rank": 4,
                "waifu": {
                    "name": "Bete Loga",
                    "original_name": "",
                    "slug": "bete-loga",
                    "image": "https://thicc.mywaifulist.moe/waifus/4662/1441c3b7f8c3ae91fe94d16756d60c6c6ba4e795f4657dabee9a4c1ea01146d5_thumb.png",
                    "popularity_rank": 1320,
                    "like_rank": 4777,
                    "trash_rank": 152,
                    "url": "https://mywaifulist.moe/waifu/bete-loga"
                }
            },
            {
                "rank": 18,
                "waifu": {
                    "name": "Sayuri Sadaoka",
                    "original_name": "一 いち ノ 瀬 せ 小 さ 百合 ゆり",
                    "slug": "sayuri-sadaoka",
                    "image": "https://thicc.mywaifulist.moe/waifus/38061/d0952841664e2f8832c947bd1c24d4caee92e52eaf42a660d96acab85c272c3a_thumb.png",
                    "popularity_rank": 13453,
                    "like_rank": 21586,
                    "trash_rank": 4714,
                    "url": "https://mywaifulist.moe/waifu/sayuri-sadaoka"
                }
            },
            {
                "rank": 19,
                "waifu": {
                    "name": "Nasrene Belt Cure",
                    "original_name": "ナスレネ・ベルト・キュール",
                    "slug": "nasrene-belt-cure-overlord",
                    "image": "https://thicc.mywaifulist.moe/waifus/19102/e2ba22ed08c8bd1f35a61947954ee85af838a2312f7e8e55ba53c386e73cbdd9_thumb.png",
                    "popularity_rank": 16798,
                    "like_rank": 24844,
                    "trash_rank": 6235,
                    "url": "https://mywaifulist.moe/waifu/nasrene-belt-cure-overlord"
                }
            },
            {
                "rank": 20,
                "waifu": {
                    "name": "Albert Ende",
                    "original_name": "アルバート・エンデ",
                    "slug": "albert-ende",
                    "image": "https://thicc.mywaifulist.moe/waifus/36817/af12d97b132cfe734dd51d473704d94008d03680b0e60d1125f4574757bcbd97_thumb.png",
                    "popularity_rank": 25044,
                    "like_rank": 33841,
                    "trash_rank": 10116,
                    "url": "https://mywaifulist.moe/waifu/albert-ende"
                }
            }
        ]
    }
}
```

This endpoint returns the ranking of the worst waifus for the current season in MyWaifuList.

## Get Airing Anime of the Season

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/airing/current`

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "title": "Summer 2022 Anime",
        "anime": [
            {
                "name": "Alternate World Pharmacy",
                "original_name": "異世界薬局",
                "slug": "alternate-world-pharmacy",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6374/096b0a4bad235b05f4aa72b4653db13adfa2cfac7431d7fb5480716a044b26a0_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/alternate-world-pharmacy"
            },
            {
                "name": "Black Summoner",
                "original_name": "リコリス・リコイル",
                "slug": "black-summoner",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6368/47498a98353bb96e88710062815ca617cf037e8a25c7700e2457266441752ea6_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/black-summoner"
            },
            {
                "name": "Call of the Night",
                "original_name": "よふかしのうた",
                "slug": "call-of-the-night",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6345/ae3516a91d0a1cc54fb0254ae03ebc8ddf35fd2c4a40ccb7d25ecfaa77db1dd5_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/call-of-the-night"
            },
            {
                "name": "Cardfight!! Vanguard: Will+Dress",
                "original_name": "カードファイト!! ヴァンガード will+Dress",
                "slug": "cardfight-vanguard-will-dress",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6364/1217068704fc6fda839c7699752099c481d268e393704a8f5daf3b0d3ee3bcdc_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/cardfight-vanguard-will-dress"
            },
            {
                "name": "Classroom of the Elite 2nd Season",
                "original_name": "ようこそ実力至上主義の教室へ 2期",
                "slug": "classroom-of-the-elite-2nd-season",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6370/406d810424e61c87b134dd083d0893401b44a9ac118827a8cd9fa6e03b6de9ec_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/classroom-of-the-elite-2nd-season"
            },
            {
                "name": "Compulsive Gambler Twin",
                "original_name": "賭ケグルイ双",
                "slug": "compulsive-gambler-twin",
                "type": "ONA",
                "image": "https://thicc.mywaifulist.moe/series/6380/b70096fdb46d5712d34e1db6d56feb912cd5e6955208b9d58d623105cbdca3fb_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/compulsive-gambler-twin"
            },
            {
                "name": "Shine Post",
                "original_name": "シャインポスト",
                "slug": "shine-post",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6223/def37f8e29477d3f277eb52c85a41a414d7a0ddc6f2498c86c839b0cf75f1509_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/shine-post"
            },
            {
                "name": "Shoot! Goal to the Future",
                "original_name": "シュート! Goal to the Future",
                "slug": "shoot-goal-to-the-future",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6360/3cba9ffaefb3e44a2524cb8214b474b625425ab9c27c6e3157895a36cd6ca84a_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/shoot-goal-to-the-future"
            },
            {
                "name": "Slave Harem in the Labyrinth of the Other World",
                "original_name": "異世界迷宮でハーレムを",
                "slug": "slave-harem-in-the-labyrinth-of-the-other-world",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6264/5181ed7147bcebbe8d4a8a230f973c46f74c099b0e58306ef654174ed28545d7_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/slave-harem-in-the-labyrinth-of-the-other-world"
            },
            {
                "name": "Smile of the Arsnotoria the Animation",
                "original_name": "咲う アルスノトリア すんっ！",
                "slug": "smile-of-the-arsnotoria-the-animation",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6410/d848891d2526bc04973640330a5a7b314670c054be0cd1ec3b50c99776f25433_thumbnail.png",
                "url": "https://mywaifulist.moe/series/smile-of-the-arsnotoria-the-animation"
            },
            {
                "name": "Teppen!!!!!!!!!!!!!!!",
                "original_name": "てっぺんっ!!!!!!!!!!!!!!!",
                "slug": "teppen",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6369/e6c10fbde875b56eccf11f9e9dbc4aeb854ef5722749b50f2cca8538f57dbd12_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/teppen"
            },
            {
                "name": "The Devil is a Part-Timer! 2nd Season",
                "original_name": "はたらく魔王さま！",
                "slug": "the-devil-is-a-part-timer-2nd-season",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6340/4d6c88e00e3ed2175d586203613c4ffa97bdc18657dfecd4b7e469a3bcacb1f3_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/the-devil-is-a-part-timer-2nd-season"
            },
            {
                "name": "The Prince of Tennis II: U-17 World Cup",
                "original_name": "新テニスの王子様 U-17 WORLD CUP",
                "slug": "the-prince-of-tennis-ii-u-17-world-cup",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6359/51c868c20a4077aebaf215f4f8500d5b08aaf933f8a62233851181b39efbd851_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/the-prince-of-tennis-ii-u-17-world-cup"
            },
            {
                "name": "The Yakuza's Guide to Babysitting",
                "original_name": "組長娘と世話係",
                "slug": "the-yakuza-s-guide-to-babysitting",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6313/cb163c1f061dcf7bbe2c02f39620be58560b2b5449b90a2d28232dcf456e22dc_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/the-yakuza-s-guide-to-babysitting"
            },
            {
                "name": "Tokyo Mew Mew New ♡",
                "original_name": "東京ミュウミュウ にゅ～♡",
                "slug": "tokyo-mew-mew-new",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6352/ea8fa7ef86c4a819af9a5432c8cc90426c2d5b10aa12ffd7a7f28983b64af585_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/tokyo-mew-mew-new"
            },
            {
                "name": "Uncle from Another World",
                "original_name": "異世界おじさん",
                "slug": "uncle-from-another-world",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6349/8723f1799136a4b8ef6b16a82bc63cf38c0e86957834b5304c293576a1143a29_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/uncle-from-another-world"
            },
            {
                "name": "Utawarerumono: Mask of Truth",
                "original_name": "うたわれるもの 二人の白皇",
                "slug": "utawarerumono-mask-of-truth",
                "type": "TV",
                "image": "https://thicc.mywaifulist.moe/series/6353/cdddf88b667431575c90b9dd808f563c42bc487e59a5fec2c237980b440d6348_thumbnail.jpg",
                "url": "https://mywaifulist.moe/series/utawarerumono-mask-of-truth"
            }
        ]
    }
}
```

This endpoint returns the data of airing anime of the current season.

## Get Series Data by its Slug

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/series/:slug`

### Path Parameters
Parameter | Required | Description
--------- | -------- | -----------
slug     | true     | Slug of the series from MyWaifuList

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "data": {
        "name": "Nisekoi: False Love",
        "original_name": "Nisekoi",
        "romaji_name": null,
        "slug": "nisekoi-false-love",
        "type": "TV",
        "episodes": 20,
        "nsfw": false,
        "studio": null,
        "characters": [
            {
                "name": "Kirisaki Chitoge",
                "original_name": "桐崎 千棘, Ichijō Chitoge",
                "slug": "kirisaki-chitoge",
                "popularity_rank": 78,
                "like_rank": 103,
                "trash_rank": 61,
                "image": "https://thicc.mywaifulist.moe/waifus/132/b5aae2947b7f7419d9f332f07a275db6784d9100bd003fc2a4fd4f382790c7b4_thumb.png",
                "url": "https://mywaifulist.moe/waifu/kirisaki-chitoge"
            },
            {
                "name": "Kosaki Onodera",
                "original_name": "",
                "slug": "kosaki-onodera-nisekoi-false-love",
                "popularity_rank": 123,
                "like_rank": 134,
                "trash_rank": 138,
                "image": "https://thicc.mywaifulist.moe/waifus/137/e95b9668b9184e61c616bc2f9adf0fc460445b2c7b6f24cce234cd1e65798f0d_thumb.png",
                "url": "https://mywaifulist.moe/waifu/kosaki-onodera-nisekoi-false-love"
            },
            {
                "name": "Marika Tachibana",
                "original_name": "Mari; Ojou-sama",
                "slug": "marika-tachibana",
                "popularity_rank": 355,
                "like_rank": 454,
                "trash_rank": 165,
                "image": "https://thicc.mywaifulist.moe/waifus/185/86ae885139ae4233ee4713dcba4b7389484e278a7870a036ad74965cc31b2ea7_thumb.jpg",
                "url": "https://mywaifulist.moe/waifu/marika-tachibana"
            },
            {
                "name": "Seishirou Tsugumi",
                "original_name": "鶫 誠士郎",
                "slug": "seishirou-tsugumi-nisekoi-false-love",
                "popularity_rank": 247,
                "like_rank": 225,
                "trash_rank": 489,
                "image": "https://thicc.mywaifulist.moe/waifus/286/5b3429d49f7780eee0aa979efb24fd70663955d1be7a4770bbfaee9c35874f7b_thumb.jpeg",
                "url": "https://mywaifulist.moe/waifu/seishirou-tsugumi-nisekoi-false-love"
            },
            {
                "name": "Ruri Miyamoto",
                "original_name": "",
                "slug": "ruri-miyamoto",
                "popularity_rank": 1225,
                "like_rank": 1502,
                "trash_rank": 511,
                "image": "https://thicc.mywaifulist.moe/waifus/1347/f091c9178b1c2544c1c7b8c931486eaf85f93a7e65ab31c52dea89e5d72e0f6b_thumb.png",
                "url": "https://mywaifulist.moe/waifu/ruri-miyamoto"
            },
            {
                "name": "Haru Onodera",
                "original_name": "",
                "slug": "haru-onodera",
                "popularity_rank": 673,
                "like_rank": 786,
                "trash_rank": 408,
                "image": "https://thicc.mywaifulist.moe/waifus/1366/28aab552ccee51f51063896551e6e5b1f5e02a9d2e279f5042e1b62063d65bd9_thumb.jpeg",
                "url": "https://mywaifulist.moe/waifu/haru-onodera"
            },
            {
                "name": "Paula McCoy",
                "original_name": "ポーラ・マッコイ",
                "slug": "paula-mccoy",
                "popularity_rank": 2437,
                "like_rank": 2856,
                "trash_rank": 1276,
                "image": "https://thicc.mywaifulist.moe/waifus/5166/03d67db476e34f0c82fe77126102d88e846fbf748bb6f08db82a7daaa0481786_thumb.jpeg",
                "url": "https://mywaifulist.moe/waifu/paula-mccoy"
            },
            {
                "name": "Nanako Onodera",
                "original_name": "小野寺 菜々子",
                "slug": "nanako-onodera",
                "popularity_rank": 3504,
                "like_rank": 3584,
                "trash_rank": 3017,
                "image": "https://thicc.mywaifulist.moe/waifus/6274/2a9795bb628edf476626c1e8a03d86c624d0d1f8931fc0d636191dbd43e93f34_thumb.png",
                "url": "https://mywaifulist.moe/waifu/nanako-onodera"
            },
            {
                "name": "Hana Kirisaki",
                "original_name": "桐崎 華",
                "slug": "hana-kirisaki",
                "popularity_rank": 2566,
                "like_rank": 2532,
                "trash_rank": 2698,
                "image": "https://thicc.mywaifulist.moe/waifus/6279/f2a9ba72d76961d63ce1a76583bc873e859b280116cca17295cb9e665151ecbe_thumb.png",
                "url": "https://mywaifulist.moe/waifu/hana-kirisaki"
            },
            {
                "name": "Youko \"Honda\"",
                "original_name": "ホンダ",
                "slug": "youko-honda",
                "popularity_rank": 5876,
                "like_rank": 6780,
                "trash_rank": 3245,
                "image": "https://thicc.mywaifulist.moe/waifus/6345/3556af33a51f3f5822ab3583610789c02b806be20c2c4b829a7bb1033372dba8_thumb.png",
                "url": "https://mywaifulist.moe/waifu/youko-honda"
            },
            {
                "name": "Kyoko Hihara",
                "original_name": "日原 教子",
                "slug": "kyoko-hihara",
                "popularity_rank": 6072,
                "like_rank": 8491,
                "trash_rank": 2275,
                "image": "https://thicc.mywaifulist.moe/waifus/6366/f69edee8e89938eb6e4a74e0730c277ff028ad206422b8c6eb07c9cc7dfdf802_thumb.jpeg",
                "url": "https://mywaifulist.moe/waifu/kyoko-hihara"
            },
            {
                "name": "Suzu Ayakiji",
                "original_name": "彩風 涼",
                "slug": "suzu-ayakiji",
                "popularity_rank": 4656,
                "like_rank": 4975,
                "trash_rank": 3231,
                "image": "https://thicc.mywaifulist.moe/waifus/6464/e7e42ad9845c06b3a61ecc7417214c7717c201a1dcf35e888a2b37697747f90c_thumb.png",
                "url": "https://mywaifulist.moe/waifu/suzu-ayakiji"
            },
            {
                "name": "Yui Kanakura",
                "original_name": "奏倉 羽",
                "slug": "yui-kanakura-nisekoi-false-love",
                "popularity_rank": 4398,
                "like_rank": 3911,
                "trash_rank": 8597,
                "image": "https://thicc.mywaifulist.moe/waifus/23852/cdf21c3ff08b47720d4ae6a23522614136c90ff012b1766b979009f19b71aeb3_thumb.jpeg",
                "url": "https://mywaifulist.moe/waifu/yui-kanakura-nisekoi-false-love"
            },
            {
                "name": "Ichijō Raku",
                "original_name": "一条 楽",
                "slug": "ichijo-raku",
                "popularity_rank": 7044,
                "like_rank": 10178,
                "trash_rank": 2647,
                "image": "https://thicc.mywaifulist.moe/waifus/25702/d0ed994470fbb8d68e56d532602279b92afb544319f41a753bc3028774942e94_thumb.jpeg",
                "url": "https://mywaifulist.moe/waifu/ichijo-raku"
            },
            {
                "name": "Sasa Miyanagi",
                "original_name": "",
                "slug": "sasa-miyanagi",
                "popularity_rank": 17074,
                "like_rank": 15875,
                "trash_rank": 20591,
                "image": "https://thicc.mywaifulist.moe/waifus/31387/1f17fd3e981ab60eb63879a7ef0a278f4b92f7723775e47cd1304933352edfc0_thumb.png",
                "url": "https://mywaifulist.moe/waifu/sasa-miyanagi"
            },
            {
                "name": "Mikage Shinohara",
                "original_name": "",
                "slug": "mikage-shinohara",
                "popularity_rank": 17007,
                "like_rank": 16347,
                "trash_rank": 17711,
                "image": "https://thicc.mywaifulist.moe/waifus/31388/559a0f38336611e00cfa9bec0a25251896b99cec5924b695120a16e0d4185c15_thumb.jpeg",
                "url": "https://mywaifulist.moe/waifu/mikage-shinohara"
            },
            {
                "name": "Shuu Maiko",
                "original_name": "集舞妓",
                "slug": "shuu-maiko",
                "popularity_rank": 13797,
                "like_rank": 13929,
                "trash_rank": 11967,
                "image": "https://thicc.mywaifulist.moe/waifus/33065/65495019e52aa45a38fcd94694e01b4781142e64aa3b03a42cc1dcca70597c52_thumb.jpeg",
                "url": "https://mywaifulist.moe/waifu/shuu-maiko"
            },
            {
                "name": "Chika Tachibana",
                "original_name": "橘 千花",
                "slug": "chika-tachibana-nisekoi-false-love",
                "popularity_rank": 30005,
                "like_rank": 28029,
                "trash_rank": 31488,
                "image": "https://thicc.mywaifulist.moe/waifus/41773/bb77b81fba703e169e2db32245e935f1065560ad1b4bbbc247e4ba229920127f_thumb.jpg",
                "url": "https://mywaifulist.moe/waifu/chika-tachibana-nisekoi-false-love"
            },
            {
                "name": "Night",
                "original_name": null,
                "slug": "night-nisekoi-false-love",
                "popularity_rank": 30668,
                "like_rank": 30943,
                "trash_rank": 26983,
                "image": "https://thicc.mywaifulist.moe/waifus/41774/775391b9e848a1ec0271f15a010938ef7f5aea48cbca600afa17b5ed45612a5e_thumb.jpg",
                "url": "https://mywaifulist.moe/waifu/night-nisekoi-false-love"
            }
        ],
        "image": "https://thicc.mywaifulist.moe/series/94/4deb14f4a2ab2b7f04a95db39f8ba2c2a2d5a20ba73988c79f1c0195ccd0066c.jpeg",
        "description": "Raku Ichijou, a first-year student at Bonyari High School, is the sole heir to an intimidating yakuza family. Ten years ago, Raku made a promise to his childhood friend. Now, all he has to go on is a pendant with a lock, which can only be unlocked with the key which the girl took with her when they parted.\r\n\r\nNow, years later, Raku has grown into a typical teenager, and all he wants is to remain as uninvolved in his yakuza background as possible while spending his school days alongside his middle school crush Kosaki Onodera. However, when the American Bee Hive Gang invades his family's turf, Raku's idyllic romantic dreams are sent for a toss as he is dragged into a frustrating conflict: Raku is to pretend that he is in a romantic relationship with Chitoge Kirisaki, the beautiful daughter of the Bee Hive's chief, so as to reduce the friction between the two groups. Unfortunately, reality could not be farther from this whopping lie—Raku and Chitoge fall in hate at first sight, as the girl is convinced he is a pathetic pushover, and in Raku's eyes, Chitoge is about as attractive as a savage gorilla. \r\n\r\nNisekoi follows the daily antics of this mismatched couple who have been forced to get along for the sake of maintaining the city's peace. With many more girls popping up his life, all involved with Raku's past somehow, his search for the girl who holds his heart and his promise leads him in more unexpected directions than he expects.\r\n\r\n[Written by MAL Rewrite]",
        "url": "https://mywaifulist.moe/series/nisekoi-false-love"
    }
}
```

## Series Search By Name

### HTTP Request
`GET https://reina-api.vercel.app/api/mwl/series`

### Query Parameters
Parameter | Required | Description
--------- | -------- | -----------
q        | false     | Name of the series to search
page     | false     | Page of the series search

> The reponse schema would be like this:

```JSON
{
    "status": 200,
    "error": false,
    "message": "Success",
    "pagination": {
        "current_page": 1,
        "total_pages": 259,
        "has_next_page": true
    },
    "data": [
        {
            "name": ".Hack Series",
            "studio": "BEE TRAIN Production Inc.",
            "original_name": null,
            "type": "TV",
            "slug": "hack-series",
            "image": "https://thicc.mywaifulist.moe/series/10/10/5ad885494ddc48a082b1fce234913f9ca0d79166dde7b84c20355a28341d645c_thumbnail.jpeg",
            "url": "https://mywaifulist.moe/series/hack-series"
        },
        {
            "name": ".hack//Legend Of The Twilight",
            "studio": "BEE TRAIN Production Inc.",
            "original_name": ".hack//Tasogare no Udewa Densetsu, .hack//黄昏の腕輪伝説",
            "type": "TV",
            "slug": "hack-legend-of-the-twilight",
            "image": "https://thicc.mywaifulist.moe/series/4763/3f3488690855b5a2e3313c8ce4fd873d62fe3d0bdd09a50095240b2d451d1998_thumbnail.jpeg",
            "url": "https://mywaifulist.moe/series/hack-legend-of-the-twilight"
        },
        {
            "name": "'Tis Time for \"Torture,\" Princess",
            "studio": null,
            "original_name": "Hime-sama, \"Goumon\" no Jikan desu, 姫様“拷問”の時間です",
            "type": "Manga",
            "slug": "tis-time-for-torture-princess",
            "image": "https://thicc.mywaifulist.moe/series/5131/25dd556eaa8af867325400056c779c1e1bbbf7c56214eae3e726a16f543170e5_thumbnail.jpeg",
            "url": "https://mywaifulist.moe/series/tis-time-for-torture-princess"
        },
        {
            "name": "[Under Lip] Oyako Neburi ～Sasou Hitozuma ･ Dakaretai Oyako～",
            "studio": null,
            "original_name": "[アンダーリップ] 母娘ねぶり～誘う人妻・抱かれたい母娘～",
            "type": "Game",
            "slug": "under-lip-oyako-neburi-sasou-hitozuma-dakaretai-oyako",
            "image": "https://thicc.mywaifulist.moe/series/4951/c517dc3dbbba1944c36b653fd7246b7753a540fcff3cff5d332f268eca1d54b2_thumbnail.png",
            "url": "https://mywaifulist.moe/series/under-lip-oyako-neburi-sasou-hitozuma-dakaretai-oyako"
        },
        {
            "name": "/Blush-DC: Hi♥mitsu",
            "studio": null,
            "original_name": "/Blush-DC～秘♥蜜～",
            "type": "Manga",
            "slug": "blush-dc-hi-mitsu",
            "image": "https://thicc.mywaifulist.moe/series/4746/c118aa00f7ea8071935bb5da88331a54052e30fdbb84ef0e9b5a1e2876f6908a_thumbnail.jpeg",
            "url": "https://mywaifulist.moe/series/blush-dc-hi-mitsu"
        },
        {
            "name": "07 Ghost",
            "studio": "Studio Deen",
            "original_name": "セブンゴースト",
            "type": "TV",
            "slug": "07-ghost",
            "image": "https://thicc.mywaifulist.moe/series/2081/12859e3dbe984cedf24011c9d854f7720ae26e53abf26761735be93a6cfd4d12_thumbnail.jpeg",
            "url": "https://mywaifulist.moe/series/07-ghost"
        },
        {
            "name": "10 Billion Wives",
            "studio": null,
            "original_name": null,
            "type": "Game",
            "slug": "10-billion-wives",
            "image": null,
            "url": "https://mywaifulist.moe/series/10-billion-wives"
        },
        {
            "name": "22/7",
            "studio": "A-1 Pictures Inc.",
            "original_name": null,
            "type": "TV",
            "slug": "22-7",
            "image": "https://thicc.mywaifulist.moe/series/4405/40ecab2b55fd00cd785251960c96593986c868666f1e754ec4bfaec6c08c7790_thumbnail.jpeg",
            "url": "https://mywaifulist.moe/series/22-7"
        },
        {
            "name": "25-sai no Joshikousei",
            "studio": null,
            "original_name": "25歳の女子高生",
            "type": "TV",
            "slug": "25-sai-no-joshikousei",
            "image": "https://thicc.mywaifulist.moe/series/2732/53afee68dc22a08269e48051eb60303db6c950df7f5cf2d7c817de8eabbbfa41_thumbnail.jpeg",
            "url": "https://mywaifulist.moe/series/25-sai-no-joshikousei"
        }
    ]
}
```