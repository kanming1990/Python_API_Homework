 
Read me_ city weather
Last Checkpoint: 30 minutes ago
(autosaved)
 
Logout 

Python [default]  

Not Trusted
File
Edit
View
Insert
Cell
Kernel
Help







Run






In [ ]:


​



In [1]:


from citipy import citipy
import random
import pandas  as pd
# pick range
indices1 = random.sample(list(range(-40,100)), 50)
indices1
​
​


Out[1]:
[44,
 4,
 75,
 92,
 5,
 23,
 1,
 85,
 65,
 -35,
 40,
 49,
 53,
 -5,
 19,
 -31,
 96,
 -34,
 16,
 45,
 2,
 29,
 -15,
 73,
 -3,
 -23,
 36,
 54,
 93,
 -2,
 98,
 -27,
 99,
 8,
 94,
 -39,
 -13,
 41,
 28,
 61,
 -8,
 -6,
 -18,
 -22,
 66,
 -25,
 87,
 48,
 74,
 84]
In [2]:


indices2 = random.sample(list(range(0,160)), 30)
indices2


Out[2]:
[85,
 5,
 111,
 154,
 157,
 45,
 122,
 61,
 51,
 11,
 131,
 55,
 103,
 117,
 147,
 135,
 120,
 80,
 60,
 65,
 138,
 145,
 4,
 33,
 38,
 130,
 50,
 140,
 59,
 52]
In [3]:


# run two variable to find city
Citylist=[]
Citylist1=[]
for x in indices1:
    for y in indices2:
        city = citipy.nearest_city(x, y) 
        Citylist= city.city_name
        Citylist1.append(Citylist)
print(Citylist1)



['kuytun', 'carpentras', 'erenhot', 'sentyabrskiy', 'severo-kurilsk', 'galyugayevskaya', 'tongliao', 'karauzyak', 'aktau', 'montale', 'dongning', 'beyneu', 'hovd', 'mujiayingzi', 'otradnoye', 'kavalerovo', 'chifeng', 'zharkent', 'karauzyak', 'tasbuget', 'terney', 'shibetsu', 'ales', 'uhlove', 'divnomorskoye', 'ningan', 'fort-shevchenko', 'yoichi', 'kegayli', 'shetpe', 'hambantota', 'yenagoa', 'sibu', 'kavieng', 'namatanai', 'xuddur', 'latung', 'victoria', 'hobyo', 'monatele', 'kloulklubed', 'eyl', 'kuantan', 'sembakung', 'lorengau', 'kloulklubed', 'manuk mangkaw', 'weligama', 'victoria', 'mahibadhoo', 'airai', 'lorengau', 'warri', 'torit', 'mega', 'ternate', 'hobyo', 'airai', 'victoria', 'hobyo', 'dikson', 'barentsburg', 'saskylakh', 'chokurdakh', 'cherskiy', 'belushya guba', 'tiksi', 'amderma', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'amderma', 'amderma', 'nizhneyansk', 'chokurdakh', 'barentsburg', 'vardo', 'tumannyy', 'tiksi', 'belushya guba', 'nizhneyansk', 'amderma', 'belushya guba', 'dikson', 'barentsburg', 'saskylakh', 'chokurdakh', 'chokurdakh', 'belushya guba', 'tiksi', 'belushya guba', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'belushya guba', 'amderma', 'nizhneyansk', 'chokurdakh', 'barentsburg', 'berlevag', 'vardo', 'tiksi', 'belushya guba', 'nizhneyansk', 'belushya guba', 'belushya guba', 'wattegama', 'warri', 'bintulu', 'kavieng', 'kavieng', 'xuddur', 'tabialan', 'victoria', 'hobyo', 'bafia', 'kloulklubed', 'eyl', 'marang', 'keningau', 'lorengau', 'kloulklubed', 'parangan', 'weligama', 'bandarbeyla', 'ugoofaaru', 'airai', 'lorengau', 'lagos', 'kapoeta', 'yabelo', 'pundaguitan', 'hobyo', 'airai', 'bandarbeyla', 'hobyo', 'khunti', 'tessalit', 'nandu', 'katsuura', 'hasaki', 'riyadh', 'yuli', 'sur', 'abu samrah', 'gat', 'nishihara', 'abu dhabi', 'gejiu', 'haimen', 'katsuura', 'naze', 'tainan', 'barela', 'sur', 'ormara', 'naze', 'katsuura', 'tessalit', 'aswan', 'jiddah', 'nishihara', 'abu samrah', 'shingu', 'qurayyat', 'abu samrah', 'hambantota', 'abonnema', 'sri aman', 'kavieng', 'namatanai', 'barawe', 'gorontalo', 'victoria', 'hobyo', 'aconibe', 'sorong', 'victoria', 'pontian kecil', 'bontang', 'lorengau', 'manokwari', 'palu', 'matara', 'victoria', 'thinadhoo', 'biak', 'lorengau', 'yenagoa', 'kamuli', 'maua', 'sorong', 'hobyo', 'vanimo', 'victoria', 'hobyo', 'dikson', 'barentsburg', 'saskylakh', 'chokurdakh', 'cherskiy', 'belushya guba', 'tiksi', 'amderma', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'amderma', 'amderma', 'nizhneyansk', 'chokurdakh', 'barentsburg', 'berlevag', 'vardo', 'tiksi', 'belushya guba', 'nizhneyansk', 'belushya guba', 'belushya guba', 'krasnoselkup', 'roald', 'aykhal', 'srednekolymsk', 'omsukchan', 'leshukonskoye', 'vilyuysk', 'verkhnyaya inta', 'ust-tsilma', 'rorvik', 'borogontsy', 'izhma', 'tura', 'nyurba', 'myaundzha', 'khandyga', 'verkhnevilyuysk', 'urengoy', 'inta', 'muzhi', 'khandyga', 'artyk', 'larsnes', 'loukhi', 'onega', 'namtsy', 'koslan', 'ust-nera', 'synya', 'ust-tsilma', 'geraldton', 'saldanha', 'busselton', 'nelson bay', 'nelson bay', 'tsihombe', 'esperance', 'saint-philippe', 'taolanaro', 'saldanha', 'flinders', 'taolanaro', 'busselton', 'albany', 'wagga wagga', 'port lincoln', 'albany', 'bambous virieux', 'saint-philippe', 'souillac', 'adelaide', 'deniliquin', 'luderitz', 'umzimvubu', 'richards bay', 'flinders', 'taolanaro', 'murray bridge', 'saint-philippe', 'taolanaro', 'korla', 'mahon', 'dongsheng', 'sentyabrskiy', 'sentyabrskiy', 'zangakatun', 'xiongyue', 'gazojak', 'gurgan', 'tortoli', 'khasan', 'balkanabat', 'jinchang', 'shunyi', 'nemuro', 'preobrazheniye', 'qinhuangdao', 'aksu', 'hazorasp', 'navoi', 'oga', 'kushiro', 'mahon', 'ankara', 'susehri', 'khasan', 'zig', 'tenno', 'dasoguz', 'gurgan', 'zyryanovsk', 'bar-le-duc', 'kyra', 'severo-kurilsk', 'severo-kurilsk', 'dubovka', 'zalantun', 'svetlyy', 'inderborskiy', 'treuchtlingen', 'obluche', 'shubarkuduk', 'bulgan', 'zabaykalsk', 'vostok', 'litovko', 'hailar', 'ayagoz', 'dombarovskiy', 'derzhavinsk', 'gurskoye', 'poronaysk', 'epernay', 'pryyutivka', 'kreminna', 'arkhara', 'aleksandrov gay', 'mayskiy', 'emba', 'inderborskiy', 'troitskoye', 'anna paulowna', 'sosnovo-ozerskoye', 'oktyabrskiy', 'ust-bolsheretsk', 'zasechnoye', 'yerofey pavlovich', 'kartaly', 'utevka', 'dannenberg', 'fevralsk', 'sharlyk', 'cheremkhovo', 'bukachacha', 'katangli', 'sofiysk', 'klyuchevskiy', 'blagoveshchenka', 'yuzhnyy', 'kushmurun', 'imeni poliny osipenko', 'tungor', 'den helder', 'mglin', 'yefremov', 'fevralsk', 'samara', 'mago', 'kizilskoye', 'koltubanovskiy', 'hambantota', 'omboue', 'jati', 'kokopo', 'kieta', 'lamu', 'katobu', 'victoria', 'victoria', 'loandjili', 'tual', 'victoria', 'lahat', 'galesong', 'madang', 'nabire', 'sinjai', 'hithadhoo', 'victoria', 'hithadhoo', 'nabire', 'madang', 'omboue', 'tabora', 'magomeni', 'amahai', 'victoria', 'kiunga', 'victoria', 'victoria', 'gopalpur', 'arlit', 'wanning', 'katsuura', 'butaritari', 'najran', 'san vicente', 'sur', 'salalah', 'bilma', 'itoman', 'salalah', 'phonhong', 'puro', 'airai', 'nishihara', 'davila', 'allapalli', 'sur', 'dwarka', 'airai', 'airai', 'kidal', 'marawi', 'tawkar', 'hirara', 'salalah', 'airai', 'sur', 'salalah', 'bambous virieux', 'luderitz', 'geraldton', 'nambucca heads', 'coffs harbour', 'tsihombe', 'esperance', 'saint-philippe', 'taolanaro', 'oranjemund', 'flinders', 'saint-joseph', 'geraldton', 'northam', 'dubbo', 'flinders', 'northam', 'bambous virieux', 'saint-philippe', 'mahebourg', 'port augusta', 'griffith', 'luderitz', 'durban', 'richards bay', 'flinders', 'taolanaro', 'broken hill', 'saint-philippe', 'taolanaro', 'dikson', 'barentsburg', 'saskylakh', 'chokurdakh', 'chokurdakh', 'belushya guba', 'tiksi', 'belushya guba', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'belushya guba', 'amderma', 'nizhneyansk', 'chokurdakh', 'barentsburg', 'longyearbyen', 'vardo', 'tiksi', 'belushya guba', 'nizhneyansk', 'belushya guba', 'belushya guba', 'geraldton', 'luderitz', 'busselton', 'nelson bay', 'port macquarie', 'tsihombe', 'esperance', 'saint-philippe', 'taolanaro', 'saldanha', 'flinders', 'taolanaro', 'busselton', 'collie', 'leeton', 'port lincoln', 'esperance', 'bambous virieux', 'saint-philippe', 'souillac', 'port pirie', 'griffith', 'luderitz', 'margate', 'richards bay', 'flinders', 'taolanaro', 'murray bridge', 'saint-philippe', 'taolanaro', 'yarada', 'tahoua', 'quang ngai', 'kavieng', 'kavieng', 'sayyan', 'dumabato', 'sur', 'salalah', 'goure', 'alugan', 'salalah', 'kosum phisai', 'aloleng', 'airai', 'airai', 'paitan', 'addanki', 'salalah', 'mangrol', 'airai', 'airai', 'tahoua', 'khartoum', 'barentu', 'alugan', 'salalah', 'airai', 'salalah', 'salalah', 'kuytun', 'romans-sur-isere', 'erenhot', 'sentyabrskiy', 'severo-kurilsk', 'urozhaynoye', 'taonan', 'kazalinsk', 'fort-shevchenko', 'mirandola', 'hengshan', 'beyneu', 'hovd', 'chifeng', 'kurilsk', 'krasnorechenskiy', 'wulanhaote', 'sarkand', 'karauzyak', 'tasbuget', 'terney', 'abashiri', 'firminy', 'zaozerne', 'krymsk', 'chaihe', 'fort-shevchenko', 'wakkanai', 'karauzyak', 'shetpe', 'hambantota', 'yenagoa', 'kuching', 'kavieng', 'namatanai', 'afgoye', 'gorontalo', 'victoria', 'hobyo', 'anisoc', 'sorong', 'victoria', 'yong peng', 'tarakan', 'lorengau', 'manokwari', 'tarakan', 'matara', 'victoria', 'kudahuvadhoo', 'biak', 'lorengau', 'yenagoa', 'lira', 'marsabit', 'ternate', 'hobyo', 'vanimo', 'victoria', 'hobyo', 'pokhara', 'warqla', 'dayong', 'hasaki', 'hasaki', 'doha', 'jiaojiang', 'khash', 'bushehr', 'nalut', 'naze', 'darab', 'leshan', 'jingdezhen', 'katsuura', 'muroto', 'choucheng', 'khatima', 'khash', 'kharan', 'shingu', 'katsuura', 'warqla', 'suez', 'tabuk', 'naze', 'bushehr', 'shimoda', 'bam', 'kazerun', 'hithadhoo', 'namibe', 'boyolangu', 'samarai', 'honiara', 'mahajanga', 'broome', 'grand gaube', 'antalaha', 'namibe', 'katherine', 'antalaha', 'palabuhanratu', 'port hedland', 'cairns', 'ngukurr', 'broome', 'hithadhoo', 'cap malheureux', 'grand gaube', 'alyangula', 'mareeba', 'namibe', 'chadiza', 'nampula', 'port keats', 'antalaha', 'alyangula', 'cap malheureux', 'antalaha', 'karaul', 'sorland', 'saskylakh', 'srednekolymsk', 'cherskiy', 'kamenka', 'zhigansk', 'amderma', 'belushya guba', 'gravdal', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'amderma', 'amderma', 'nizhneyansk', 'chokurdakh', 'sorland', 'vardo', 'tumannyy', 'tiksi', 'belushya guba', 'deputatskiy', 'amderma', 'belushya guba', 'hambantota', 'port-gentil', 'pangkalanbuun', 'namatanai', 'kieta', 'kismayo', 'kendari', 'victoria', 'victoria', 'tchibanga', 'amahai', 'victoria', 'curup', 'barabai', 'lorengau', 'nabire', 'rantepao', 'hithadhoo', 'victoria', 'hithadhoo', 'nabire', 'angoram', 'port-gentil', 'misasi', 'taveta', 'amahai', 'victoria', 'vanimo', 'victoria', 'victoria', 'hithadhoo', 'henties bay', 'carnarvon', 'bundaberg', 'hervey bay', 'sakaraha', 'port hedland', 'bambous virieux', 'manakara', 'henties bay', 'yulara', 'saint-joseph', 'carnarvon', 'roebourne', 'emerald', 'alice springs', 'port hedland', 'grand river south east', 'mahebourg', 'bambous virieux', 'mount isa', 'charters towers', 'henties bay', 'chokwe', 'inhambane', 'yulara', 'manakara', 'mount isa', 'souillac', 'saint-leu', 'korla', 'tazmalt', 'houma', 'sentyabrskiy', 'sentyabrskiy', 'piranshahr', 'wencheng', 'sarakhs', 'karaj', 'lamtah', 'hamada', 'shahrud', 'linxia', 'taian', 'kamaishi', 'toyooka', 'jiaonan', 'leh', 'mashhad', 'dawlatabad', 'tatsuno', 'hasaki', 'tazmalt', 'anamur', 'manbij', 'nagato', 'qazvin', 'mitsukaido', 'neyshabur', 'damavand', 'zalesovo', 'harlingen', 'kurumkan', 'sobolevo', 'sobolevo', 'zykovo', 'yerofey pavlovich', 'plast', 'sergiyevsk', 'neustadt', 'stoyba', 'rayevskiy', 'ust-uda', 'bukachacha', 'ekhabi', 'chumikan', 'mogocha', 'pankrushikha', 'uyskoye', 'zverinogolovskoye', 'mnogovershinnyy', 'ekhabi', 'den helder', 'roslavl', 'brusyanskiy', 'fevralsk', 'novaya malykla', 'mnogovershinnyy', 'mishkino', 'kamyshla', 'dikson', 'barentsburg', 'saskylakh', 'chokurdakh', 'chokurdakh', 'belushya guba', 'tiksi', 'belushya guba', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'belushya guba', 'amderma', 'nizhneyansk', 'chokurdakh', 'barentsburg', 'berlevag', 'vardo', 'tiksi', 'belushya guba', 'nizhneyansk', 'belushya guba', 'belushya guba', 'hambantota', 'port-gentil', 'pangkalanbuun', 'namatanai', 'kieta', 'kismayo', 'luwuk', 'victoria', 'victoria', 'mouila', 'sorong', 'victoria', 'jambi', 'balikpapan', 'lorengau', 'biak', 'poso', 'hithadhoo', 'victoria', 'hithadhoo', 'biak', 'wewak', 'port-gentil', 'muriti', 'wote', 'sorong', 'victoria', 'vanimo', 'victoria', 'victoria', 'dikson', 'barentsburg', 'saskylakh', 'chokurdakh', 'chokurdakh', 'belushya guba', 'tiksi', 'belushya guba', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'belushya guba', 'amderma', 'nizhneyansk', 'chokurdakh', 'barentsburg', 'longyearbyen', 'vardo', 'tiksi', 'belushya guba', 'nizhneyansk', 'belushya guba', 'belushya guba', 'grand river south east', 'luderitz', 'carnarvon', 'bongaree', 'gold coast', 'tsihombe', 'esperance', 'souillac', 'taolanaro', 'luderitz', 'yulara', 'saint-joseph', 'carnarvon', 'geraldton', 'roma', 'alice springs', 'geraldton', 'grand river south east', 'souillac', 'mahebourg', 'alice springs', 'roma', 'luderitz', 'nsoko', 'inhambane', 'yulara', 'taolanaro', 'broken hill', 'saint-philippe', 'taolanaro', 'dikson', 'barentsburg', 'saskylakh', 'chokurdakh', 'chokurdakh', 'belushya guba', 'tiksi', 'belushya guba', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'belushya guba', 'amderma', 'nizhneyansk', 'chokurdakh', 'barentsburg', 'longyearbyen', 'vardo', 'tiksi', 'belushya guba', 'nizhneyansk', 'belushya guba', 'belushya guba', 'kalmunai', 'ila', 'phan rang', 'kavieng', 'kavieng', 'odweyne', 'siocon', 'bandarbeyla', 'eyl', 'jalingo', 'kloulklubed', 'bandarbeyla', 'sai buri', 'balabac', 'lorengau', 'airai', 'simbahan', 'anuradhapura', 'bandarbeyla', 'kavaratti', 'airai', 'lorengau', 'oyo', 'gambela', 'butajira', 'baculin', 'eyl', 'airai', 'bandarbeyla', 'bandarbeyla', 'dikson', 'barentsburg', 'saskylakh', 'chokurdakh', 'chokurdakh', 'belushya guba', 'tiksi', 'belushya guba', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'belushya guba', 'amderma', 'nizhneyansk', 'chokurdakh', 'barentsburg', 'longyearbyen', 'vardo', 'tiksi', 'belushya guba', 'nizhneyansk', 'belushya guba', 'belushya guba', 'busselton', 'saldanha', 'busselton', 'batemans bay', 'ulladulla', 'tsihombe', 'esperance', 'saint-philippe', 'taolanaro', 'cape town', 'port lincoln', 'taolanaro', 'busselton', 'albany', 'sale', 'port lincoln', 'albany', 'bambous virieux', 'saint-philippe', 'saint-philippe', 'mount gambier', 'crib point', 'saldanha', 'east london', 'margate', 'port lincoln', 'taolanaro', 'mount gambier', 'saint-philippe', 'taolanaro', 'hithadhoo', 'namibe', 'boyolangu', 'samarai', 'honiara', 'boueni', 'kupang', 'grand gaube', 'sambava', 'benguela', 'howard springs', 'sambava', 'palabuhanratu', 'praya', 'port moresby', 'milingimbi', 'waingapu', 'hithadhoo', 'cap malheureux', 'grand gaube', 'nhulunbuy', 'cairns', 'namibe', 'kasungu', 'montepuez', 'palmerston', 'ambilobe', 'nhulunbuy', 'cap malheureux', 'sambava', 'korla', 'mahon', 'hohhot', 'sentyabrskiy', 'sentyabrskiy', 'voskevan', 'yingkou', 'hazorasp', 'artyom', 'santa marinella', 'khasan', 'balkanabat', 'jinchang', 'shunyi', 'nemuro', 'preobrazheniye', 'yebaishou', 'aksu', 'dasoguz', 'nurota', 'oga', 'kushiro', 'mahon', 'safranbolu', 'ordu', 'khasan', 'nardaran', 'kizukuri', 'akdepe', 'artyom', 'kathmandu', 'warqla', 'lengshuijiang', 'hasaki', 'hasaki', 'buraydah', 'wenling', 'khash', 'khormuj', 'awbari', 'naze', 'lar', 'xichang', 'xiongshi', 'katsuura', 'kushima', 'lishui', 'pawayan', 'iranshahr', 'kharan', 'shingu', 'katsuura', 'warqla', 'hurghada', 'tabuk', 'naze', 'bushehr', 'shimoda', 'bam', 'khormuj', 'belyy yar', 'aras', 'vitim', 'talaya', 'omsukchan', 'kizema', 'vilyuysk', 'ous', 'koygorodok', 'brumunddal', 'amga', 'gayny', 'vanavara', 'suntar', 'kholodnyy', 'eldikan', 'verkhnevilyuysk', 'kargasok', 'polunochnoye', 'kommunisticheskiy', 'solnechnyy', 'okhotsk', 'aras', 'olonets', 'lipin bor', 'mayya', 'vizinga', 'solnechnyy', 'cheremukhovo', 'kortkeros', 'hithadhoo', 'mayumba', 'jatiroto', 'buin', 'gizo', 'mitsamiouli', 'maumere', 'victoria', 'ambilobe', 'soyo', 'tual', 'victoria', 'labuhan', 'sumbawa', 'wau', 'tual', 'ruteng', 'hithadhoo', 'victoria', 'victoria', 'merauke', 'kerema', 'gamba', 'mlowo', 'kisanga', 'tual', 'ambilobe', 'merauke', 'victoria', 'victoria', 'hambantota', 'gamba', 'jati', 'panguna', 'kieta', 'micheweni', 'katobu', 'victoria', 'victoria', 'cabinda', 'tual', 'victoria', 'pringsewu', 'galesong', 'lae', 'tual', 'tanete', 'hithadhoo', 'victoria', 'victoria', 'kiunga', 'kundiawa', 'omboue', 'sikonge', 'lugoba', 'tual', 'victoria', 'kiunga', 'victoria', 'victoria', 'hithadhoo', 'namibe', 'karratha', 'mackay', 'poum', 'tsiroanomandidy', 'broome', 'grand gaube', 'ambodifototra', 'opuwo', 'kununurra', 'saint-denis', 'palabuhanratu', 'karratha', 'ingham', 'ngukurr', 'broome', 'hithadhoo', 'grand gaube', 'quatre cocos', 'mount isa', 'atherton', 'namibe', 'manica', 'quelimane', 'kununurra', 'toamasina', 'mount isa', 'grand gaube', 'ambodifototra', 'hithadhoo', 'henties bay', 'carnarvon', 'gladstone', 'hervey bay', 'beroroha', 'port hedland', 'bambous virieux', 'mananjary', 'henties bay', 'yulara', 'saint-pierre', 'carnarvon', 'roebourne', 'moranbah', 'alice springs', 'port hedland', 'grand river south east', 'bambous virieux', 'grand river south east', 'mount isa', 'charters towers', 'henties bay', 'chiredzi', 'inhambane', 'yulara', 'mananjary', 'mount isa', 'mahebourg', 'saint-leu', 'igarka', 'roald', 'aykhal', 'srednekolymsk', 'srednekolymsk', 'mezen', 'zhigansk', 'verkhnyaya inta', 'ust-tsilma', 'rorvik', 'batagay-alyta', 'izhma', 'tura', 'nyurba', 'belaya gora', 'batagay', 'verkhnevilyuysk', 'urengoy', 'inta', 'muzhi', 'batagay', 'artyk', 'roald', 'loukhi', 'onega', 'batagay-alyta', 'ust-tsilma', 'khonuu', 'inta', 'ust-tsilma', 'hithadhoo', 'henties bay', 'carnarvon', 'hervey bay', 'hervey bay', 'beloha', 'port hedland', 'mahebourg', 'vangaindrano', 'walvis bay', 'yulara', 'saint-joseph', 'carnarvon', 'carnarvon', 'emerald', 'alice springs', 'port hedland', 'grand river south east', 'souillac', 'bambous virieux', 'alice springs', 'emerald', 'henties bay', 'macia', 'inhambane', 'yulara', 'vangaindrano', 'mount isa', 'souillac', 'vangaindrano', 'dikson', 'barentsburg', 'saskylakh', 'chokurdakh', 'chokurdakh', 'belushya guba', 'tiksi', 'amderma', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'belushya guba', 'amderma', 'nizhneyansk', 'chokurdakh', 'barentsburg', 'berlevag', 'vardo', 'tiksi', 'belushya guba', 'nizhneyansk', 'belushya guba', 'belushya guba', 'zaysan', 'chaumont', 'ondorhaan', 'severo-kurilsk', 'severo-kurilsk', 'malyye derbety', 'zalantun', 'kazalinsk', 'inderborskiy', 'landsberg', 'amurzet', 'makat', 'bulgan', 'manzhouli', 'vostok', 'khor', 'hailar', 'ayagoz', 'emba', 'dzhusaly', 'svetlaya', 'poronaysk', 'saint-andre-les-vergers', 'kazanka', 'vysoke', 'xinqing', 'inderborskiy', 'sovetskaya gavan', 'emba', 'inderborskiy', 'karaul', 'sorland', 'saskylakh', 'srednekolymsk', 'cherskiy', 'belushya guba', 'tiksi', 'amderma', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'amderma', 'amderma', 'nizhneyansk', 'chokurdakh', 'sorland', 'vardo', 'tumannyy', 'tiksi', 'belushya guba', 'nizhneyansk', 'amderma', 'belushya guba', 'dikson', 'barentsburg', 'saskylakh', 'chokurdakh', 'cherskiy', 'belushya guba', 'tiksi', 'amderma', 'belushya guba', 'barentsburg', 'tiksi', 'belushya guba', 'khatanga', 'saskylakh', 'chokurdakh', 'nizhneyansk', 'saskylakh', 'dikson', 'amderma', 'amderma', 'nizhneyansk', 'chokurdakh', 'barentsburg', 'berlevag', 'vardo', 'tiksi', 'belushya guba', 'nizhneyansk', 'belushya guba', 'belushya guba']
In [4]:


​
CITY_500 = pd.DataFrame({"City":Citylist1})
CITY_500.head()


Out[4]:

City
0
kuytun
1
carpentras
2
erenhot
3
sentyabrskiy
4
severo-kurilsk
In [5]:


#count double
city_list_no_depulicate =CITY_500["City"].value_counts()
​
city_list_no_depulicate.head(800)
​


Out[5]:
belushya guba        81
victoria             47
chokurdakh           41
saskylakh            36
nizhneyansk          35
tiksi                35
barentsburg          31
amderma              26
dikson               22
hithadhoo            18
taolanaro            18
airai                16
saint-philippe       14
vardo                12
khatanga             12
lorengau             12
hobyo                12
salalah              10
bambous virieux      10
carnarvon             9
kavieng               9
henties bay           8
luderitz              8
katsuura              8
yulara                8
sentyabrskiy          8
port hedland          7
mount isa             7
souillac              7
hambantota            7
                     ..
sai buri              1
utevka                1
vizinga               1
gravdal               1
zaysan                1
siocon                1
torit                 1
barentu               1
deniliquin            1
gopalpur              1
myaundzha             1
moranbah              1
phonhong              1
kommunisticheskiy     1
koslan                1
cheremkhovo           1
balikpapan            1
belyy yar             1
goure                 1
makat                 1
ankara                1
cheremukhovo          1
kizema                1
aconibe               1
yoichi                1
barawe                1
barela                1
abonnema              1
dubovka               1
batemans bay          1
Name: City, Length: 626, dtype: int64
In [6]:


# get city list
CITY_500_2 = pd.DataFrame({"the numbers of time being picked":city_list_no_depulicate})
​
​
CITY_500_2.index.name="City"
CITY_500_2.reset_index(level=0, inplace=True)
​
CITY_500_2.head()
​


Out[6]:

City
the numbers of time being picked
0
belushya guba
81
1
victoria
47
2
chokurdakh
41
3
saskylakh
36
4
nizhneyansk
35
In [7]:


CITY_500_2.to_csv('cities.csv')




#convert city to city list Final_city_List=CITY_500_2["City"] Final_city_List2=list(Final_city_List)
In [9]:


# Dependencies
import csv
import matplotlib.pyplot as plt
import openweathermapy as owm
import pandas as pd
import pprint as pprint
​
# import api_key from config file
api_key = "59d7894fce978fbab09b1fd2bd93da2f"



In [10]:


settings = {"units": "metric", "appid": api_key}



In [11]:


weather_data = []
​
for i, city in enumerate(Final_city_List2):
    try:
        weather_data.append(owm.get_current(city, **settings))
    except:
        print("Hey Error here!", i, city)
        continue
        
    



Hey Error here! 0 belushya guba
Hey Error here! 4 nizhneyansk
Hey Error here! 6 barentsburg
Hey Error here! 7 amderma
Hey Error here! 10 taolanaro
Hey Error here! 25 sentyabrskiy
Hey Error here! 41 grand river south east
Hey Error here! 53 inderborskiy
Hey Error here! 54 tsihombe
Hey Error here! 58 warqla
Hey Error here! 65 karauzyak
Hey Error here! 80 tumannyy
Hey Error here! 84 palabuhanratu
Hey Error here! 97 korla
Hey Error here! 98 fevralsk
Hey Error here! 104 artyk
Hey Error here! 118 karaul
Hey Error here! 120 kazalinsk
Hey Error here! 121 khormuj
Hey Error here! 143 ngukurr
Hey Error here! 144 tasbuget
Hey Error here! 148 kismayo
Hey Error here! 179 gurgan
Hey Error here! 193 ambodifototra
Hey Error here! 204 stoyba
Hey Error here! 207 jiaojiang
Hey Error here! 208 ust-bolsheretsk
Hey Error here! 241 xiongshi
Hey Error here! 244 kushmurun
Hey Error here! 247 monatele
Hey Error here! 262 sofiysk
Hey Error here! 271 dzhusaly
Hey Error here! 287 leshan
Hey Error here! 306 svetlyy
Hey Error here! 309 jiddah
Hey Error here! 310 taian
Hey Error here! 312 kyra
Hey Error here! 314 kegayli
Hey Error here! 334 sumbawa
Hey Error here! 336 marang
Hey Error here! 344 choucheng
Hey Error here! 351 eldikan
Hey Error here! 376 chokwe
Hey Error here! 382 tawkar
Hey Error here! 388 kapoeta
Hey Error here! 389 khonuu
Hey Error here! 396 wulanhaote
Hey Error here! 416 krasnoselkup
Hey Error here! 427 milingimbi
Hey Error here! 431 ningan
Hey Error here! 453 qurayyat
Hey Error here! 469 afgoye
Hey Error here! 470 gurskoye
Hey Error here! 505 tabialan
Hey Error here! 510 umzimvubu
Hey Error here! 535 ondorhaan
Hey Error here! 540 odweyne
Hey Error here! 551 wau
Hey Error here! 560 obluche
Hey Error here! 564 hurghada
Hey Error here! 582 phan rang
Hey Error here! 602 torit
Hey Error here! 621 barawe
In [ ]:


​
​
​



In [ ]:


​



In [12]:


column_names = ["name","main_temp", "coord_lat", "coord_lon","main_humidity","wind_speed","clouds_all"]
summary = ["name","main.temp", "coord.lat", "coord.lon","main.humidity","wind.speed","clouds.all"]
​
# Create a Pandas DataFrame with the results
data = [response(*summary) for response in weather_data ]
​
weather_data = pd.DataFrame(data,columns=column_names)
weather_data.head(5)


Out[12]:

name
main_temp
coord_lat
coord_lon
main_humidity
wind_speed
clouds_all
0
Victoria
30.00
5.28
115.24
70
1.00
75
1
Chokurdakh
-2.36
70.62
147.90
100
1.11
0
2
Saskylakh
-19.56
71.97
114.09
76
4.66
0
3
Tiksi
-13.07
71.64
128.87
81
2.16
36
4
Dikson
-22.06
73.51
80.55
95
5.31
12
In [13]:


plt.scatter(weather_data["coord_lat"], weather_data["main_temp"], marker="o", facecolors="red", edgecolors="black",
             alpha=0.75)
plt.xlabel("Latitude")
plt.ylabel("Main Temp")
plt.title("Latitude & Main Temp")
plt.savefig("Latitude & Main Temp.png")




In [14]:


plt.show()



In [15]:


plt.scatter(weather_data["coord_lat"], weather_data["main_humidity"], marker="o", facecolors="red", edgecolors="black",
             alpha=0.75)
plt.xlabel("Latitude")
plt.ylabel("main_humidity")
plt.title("Latitude & main_humidity")
plt.savefig("Latitude & main_humidity.png")




In [16]:


plt.show()



In [17]:


plt.scatter(weather_data["coord_lat"], weather_data["clouds_all"], marker="o", facecolors="red", edgecolors="black",
             alpha=0.75)
plt.xlabel("Latitude")
plt.ylabel("clouds_all")
plt.title("Latitude & clouds_all")
plt.savefig("Latitude & clouds_all.png")




In [18]:


plt.show()
​



In [19]:


plt.scatter(weather_data["coord_lat"], weather_data["wind_speed"], marker="o", facecolors="red", edgecolors="black",
             alpha=0.75)
plt.xlabel("Latitude")
plt.ylabel("wind_speed")
plt.title("Latitude & wind_speed")
plt.savefig("Latitude & wind_speed.png")




In [20]:


plt.show()



