1
00:00:00,240 --> 00:00:02,280
welcome everyone to the next iteration

2
00:00:02,280 --> 00:00:04,319
of the kaggle generative AI intensive

3
00:00:04,319 --> 00:00:06,759
course we're really excited to have over

4
00:00:06,759 --> 00:00:09,200
a quarter of a million developers dialed

5
00:00:09,200 --> 00:00:11,200
in today to learn all about the Gemini

6
00:00:11,200 --> 00:00:14,879
apis AI Studio vertex Ai and all of the

7
00:00:14,879 --> 00:00:17,080
wonderful AI features that Google cloud

8
00:00:17,080 --> 00:00:18,680
has been putting out over the last

9
00:00:18,680 --> 00:00:21,359
several months um but before we we we

10
00:00:21,359 --> 00:00:25,080
begin I really want uh to uh to welcome

11
00:00:25,080 --> 00:00:26,840
on to the stage someone very special our

12
00:00:26,840 --> 00:00:29,320
chief scientist at Google um who wanted

13
00:00:29,320 --> 00:00:31,920
to be here to to to give you a short

14
00:00:31,920 --> 00:00:34,719
message um so with that let's welcome

15
00:00:34,719 --> 00:00:36,000
Jeff

16
00:00:36,000 --> 00:00:39,559
Dean hi everyone Jeff de here uh I'm

17
00:00:39,559 --> 00:00:41,360
super excited you've all decided to join

18
00:00:41,360 --> 00:00:45,760
the kaggle Gen uh intensive uh course um

19
00:00:45,760 --> 00:00:47,360
you know we ran this course last year

20
00:00:47,360 --> 00:00:50,199
and we had about 150,000 developers sign

21
00:00:50,199 --> 00:00:52,120
up um we're running it this year looks

22
00:00:52,120 --> 00:00:53,960
like we'll have more than 200,000 which

23
00:00:53,960 --> 00:00:56,000
is pretty amazing um and really we're

24
00:00:56,000 --> 00:00:59,120
excited to see what people do with uh

25
00:00:59,120 --> 00:01:00,840
these generative model there's so many

26
00:01:00,840 --> 00:01:03,199
possibilities in terms of creating you

27
00:01:03,199 --> 00:01:06,000
know useful uh things that help people

28
00:01:06,000 --> 00:01:07,720
get things done you know things that

29
00:01:07,720 --> 00:01:10,040
entertain people things that help people

30
00:01:10,040 --> 00:01:11,600
you know take information and transform

31
00:01:11,600 --> 00:01:15,000
it into different kinds of modalities um

32
00:01:15,000 --> 00:01:16,880
and the the capabilities of these models

33
00:01:16,880 --> 00:01:19,680
are increasing quickly so that means

34
00:01:19,680 --> 00:01:21,240
that the building blocks that we all

35
00:01:21,240 --> 00:01:24,240
have as developers are growing in uh you

36
00:01:24,240 --> 00:01:26,159
know sophistication and that enable us

37
00:01:26,159 --> 00:01:28,000
to do more and more interesting things

38
00:01:28,000 --> 00:01:29,920
so we're really really excited about

39
00:01:29,920 --> 00:01:31,640
what you all are going to do uh what

40
00:01:31,640 --> 00:01:33,640
you're all going to learn to do and

41
00:01:33,640 --> 00:01:35,880
that's why we're running this course and

42
00:01:35,880 --> 00:01:37,720
uh we're looking forward to answering

43
00:01:37,720 --> 00:01:40,240
questions and giving you you know

44
00:01:40,240 --> 00:01:42,159
guidance about how to use these tools

45
00:01:42,159 --> 00:01:45,880
and seeing how you all use them super

46
00:01:45,880 --> 00:01:47,719
exciting thank

47
00:01:47,719 --> 00:01:50,520
you excellent and thank you so much Jeff

48
00:01:50,520 --> 00:01:54,479
Dean I I think that we all have uh uh

49
00:01:54,479 --> 00:01:56,280
we've all used many of the products that

50
00:01:56,280 --> 00:01:58,680
Jeff has built from the ground up um and

51
00:01:58,680 --> 00:02:00,920
so it's wonderful to have him here today

52
00:02:00,920 --> 00:02:03,840
to tell us a little bit about um what

53
00:02:03,840 --> 00:02:05,960
he's excited to see for our students to

54
00:02:05,960 --> 00:02:08,520
create so taking a look back at the

55
00:02:08,520 --> 00:02:11,280
slides um just as a general reminder

56
00:02:11,280 --> 00:02:13,760
this five-day intensive course is hosted

57
00:02:13,760 --> 00:02:16,000
by kaggle it includes everything from

58
00:02:16,000 --> 00:02:18,319
daily assignments to Discord discussion

59
00:02:18,319 --> 00:02:21,680
threads um live stream uh and ask me

60
00:02:21,680 --> 00:02:23,239
anything session which you're dialed

61
00:02:23,239 --> 00:02:27,080
into right now um and as a reminder um

62
00:02:27,080 --> 00:02:29,360
this 5-day generative AI intensive

63
00:02:29,360 --> 00:02:31,519
course incorporates foundational models

64
00:02:31,519 --> 00:02:33,879
embeddings and Vector databases agents

65
00:02:33,879 --> 00:02:36,599
domain specific models and today we are

66
00:02:36,599 --> 00:02:38,720
going to be exploring the wonderful

67
00:02:38,720 --> 00:02:41,519
world of foundational models and prompt

68
00:02:41,519 --> 00:02:44,440
engineering um just as a reminder you

69
00:02:44,440 --> 00:02:46,000
should have been listening to our

70
00:02:46,000 --> 00:02:48,000
summary podcast episode which was

71
00:02:48,000 --> 00:02:50,040
created by notebook LM we'll get to hear

72
00:02:50,040 --> 00:02:52,560
more from The Notebook lmm team later

73
00:02:52,560 --> 00:02:54,480
this week you should have taken a look

74
00:02:54,480 --> 00:02:56,319
at some of the white papers that we have

75
00:02:56,319 --> 00:02:58,840
around this first day's content and then

76
00:02:58,840 --> 00:03:00,959
also importantly the kaggle code lab

77
00:03:00,959 --> 00:03:02,599
which an aunt will be walking through

78
00:03:02,599 --> 00:03:05,680
towards the end of today um but before

79
00:03:05,680 --> 00:03:08,640
we go into this I want to have a huge

80
00:03:08,640 --> 00:03:10,799
shout out to our generative AI course

81
00:03:10,799 --> 00:03:13,080
moderators um this is the team that's

82
00:03:13,080 --> 00:03:15,040
been tirelessly answering all of the

83
00:03:15,040 --> 00:03:16,599
questions that y'all have been asking on

84
00:03:16,599 --> 00:03:18,159
Discord they've been helping spot

85
00:03:18,159 --> 00:03:19,640
questions that could be useful in the

86
00:03:19,640 --> 00:03:23,000
Q&A session um so thank you so much a

87
00:03:23,000 --> 00:03:25,680
virtual Round of Applause to everybody

88
00:03:25,680 --> 00:03:28,280
who's been um making this course happen

89
00:03:28,280 --> 00:03:30,760
if you see them digitally uh or in

90
00:03:30,760 --> 00:03:34,280
person say thank you um and with that

91
00:03:34,280 --> 00:03:37,760
let's head into our Q&A so today I am

92
00:03:37,760 --> 00:03:40,319
honored beyond belief to welcome Logan

93
00:03:40,319 --> 00:03:43,280
Kilpatrick Warren Barkley Kieran melan

94
00:03:43,280 --> 00:03:46,640
um Arena Ziggler and Matt boso to um to

95
00:03:46,640 --> 00:03:49,760
the stage um they are our expert hosts

96
00:03:49,760 --> 00:03:52,720
for day one all about prompt engineering

97
00:03:52,720 --> 00:03:57,079
and foundational models um and I I with

98
00:03:57,079 --> 00:03:59,959
that I I'm going to to go ahead and get

99
00:03:59,959 --> 00:04:04,480
into our first question um so first uh

100
00:04:04,480 --> 00:04:08,280
first question is for Logan and for Matt

101
00:04:08,280 --> 00:04:11,480
um I and taking a look at it now tell us

102
00:04:11,480 --> 00:04:15,120
a little bit about AI studio um what

103
00:04:15,120 --> 00:04:16,720
capabilities does it unlock for

104
00:04:16,720 --> 00:04:18,880
developers and how does it bridge the

105
00:04:18,880 --> 00:04:20,880
gap between Google deep mind's latest

106
00:04:20,880 --> 00:04:22,960
research and all of our great Google

107
00:04:22,960 --> 00:04:24,000
Cloud

108
00:04:24,000 --> 00:04:27,440
tools want to go first Logan yeah sure

109
00:04:27,440 --> 00:04:30,680
I'm uh I'm happy to Pig uh this is this

110
00:04:30,680 --> 00:04:32,440
is a ton of fun to tell folks about

111
00:04:32,440 --> 00:04:33,759
about AI studio and everything that

112
00:04:33,759 --> 00:04:36,000
we're doing the sort of high level

113
00:04:36,000 --> 00:04:38,160
mental model of this is aiio is intended

114
00:04:38,160 --> 00:04:40,800
to be the F the fast path to access the

115
00:04:40,800 --> 00:04:42,160
latest Gemini models the latest

116
00:04:42,160 --> 00:04:44,080
generative AI models coming out of

117
00:04:44,080 --> 00:04:45,680
Google and and specifically coming out

118
00:04:45,680 --> 00:04:47,960
of Deep Mind um so if you're a developer

119
00:04:47,960 --> 00:04:50,199
and you want to see what's possible with

120
00:04:50,199 --> 00:04:51,800
with the Gemini models and page I know

121
00:04:51,800 --> 00:04:53,880
you and I are do this all the time you

122
00:04:53,880 --> 00:04:55,280
have some idea of what you want to build

123
00:04:55,280 --> 00:04:57,280
with ai ai studio is a great place to

124
00:04:57,280 --> 00:04:59,360
just show up test can the model actually

125
00:04:59,360 --> 00:05:00,880
do this thing does it have this

126
00:05:00,880 --> 00:05:03,240
capability baked in um and then with a

127
00:05:03,240 --> 00:05:05,120
single click you can go and grab a bunch

128
00:05:05,120 --> 00:05:06,800
of code and and actually start building

129
00:05:06,800 --> 00:05:09,520
that idea um in python or JavaScript or

130
00:05:09,520 --> 00:05:11,520
whatever your language of choic is um

131
00:05:11,520 --> 00:05:13,320
you can also get an API key and and

132
00:05:13,320 --> 00:05:14,680
start building with the API really

133
00:05:14,680 --> 00:05:17,960
quickly so really sort of the the path

134
00:05:17,960 --> 00:05:20,960
to accelerate um idea to actually

135
00:05:20,960 --> 00:05:22,919
building something with Gemini

136
00:05:22,919 --> 00:05:25,360
absolutely and I know that uh just

137
00:05:25,360 --> 00:05:27,560
recently we've been focused on unifying

138
00:05:27,560 --> 00:05:30,639
the sdks such that you know when you hit

139
00:05:30,639 --> 00:05:32,240
that get code button it's a really

140
00:05:32,240 --> 00:05:35,080
seamless path to get from AI Studio code

141
00:05:35,080 --> 00:05:38,039
to code that works with vertex AI um so

142
00:05:38,039 --> 00:05:40,639
it's been really really cool to see um

143
00:05:40,639 --> 00:05:43,160
Matt is there anything you want to add

144
00:05:43,160 --> 00:05:46,240
no that's what we going say people often

145
00:05:46,240 --> 00:05:49,160
ask why we have two different products

146
00:05:49,160 --> 00:05:51,160
vertex and the I studio and Warren is

147
00:05:51,160 --> 00:05:54,080
going to talk about vertex soon but uh

148
00:05:54,080 --> 00:05:57,039
we want to have both a unified developer

149
00:05:57,039 --> 00:05:58,720
experience like you all say that you

150
00:05:58,720 --> 00:06:00,440
shouldn't have to Cho choose one or the

151
00:06:00,440 --> 00:06:02,960
other before you start coding like you

152
00:06:02,960 --> 00:06:05,319
can just you know pick an SDK and just

153
00:06:05,319 --> 00:06:07,639
work with it uh but there is value

154
00:06:07,639 --> 00:06:09,400
having two different products for two

155
00:06:09,400 --> 00:06:11,919
different types of use case I studio is

156
00:06:11,919 --> 00:06:14,919
very very simple it's not an mlops

157
00:06:14,919 --> 00:06:17,400
platform it doesn't have a model garden

158
00:06:17,400 --> 00:06:19,479
with many models right it's just

159
00:06:19,479 --> 00:06:22,520
Google's models uh is the simplest sort

160
00:06:22,520 --> 00:06:25,039
of getting started experience where

161
00:06:25,039 --> 00:06:27,000
vertex is an Enterprise product and it

162
00:06:27,000 --> 00:06:29,160
has a bunch of capabilities that AI

163
00:06:29,160 --> 00:06:32,000
Studio does not have so there is very

164
00:06:32,000 --> 00:06:33,560
having these two different things as

165
00:06:33,560 --> 00:06:35,199
long as we have a unified developer

166
00:06:35,199 --> 00:06:36,400
experience so you don't have to write

167
00:06:36,400 --> 00:06:38,599
your code twice and and we are doing

168
00:06:38,599 --> 00:06:41,160
that excellent and people can try it out

169
00:06:41,160 --> 00:06:45,280
today uh at AI dodev I believe uh that

170
00:06:45,280 --> 00:06:48,240
which is the coolest URL that uh that I

171
00:06:48,240 --> 00:06:51,520
have seen in recent so very very excited

172
00:06:51,520 --> 00:06:54,520
thank you for the great answer um second

173
00:06:54,520 --> 00:06:57,400
question for Kieran um how has prompt

174
00:06:57,400 --> 00:06:59,680
engineering evolved since the early days

175
00:06:59,680 --> 00:07:01,280
of large language models so as an

176
00:07:01,280 --> 00:07:04,120
example Palm 2 gpt3 and the like how do

177
00:07:04,120 --> 00:07:05,919
you think it will evolve over time

178
00:07:05,919 --> 00:07:07,800
especially given the rise and popularity

179
00:07:07,800 --> 00:07:09,560
for multimodal models and you've been

180
00:07:09,560 --> 00:07:12,000
doing this for quite some time I believe

181
00:07:12,000 --> 00:07:14,120
so this this is a fascinating question I

182
00:07:14,120 --> 00:07:15,759
think it's fascinating to look back at

183
00:07:15,759 --> 00:07:17,360
the evolution not just of prompt

184
00:07:17,360 --> 00:07:19,520
engineering but s of language models

185
00:07:19,520 --> 00:07:21,919
themselves um so if you look at how

186
00:07:21,919 --> 00:07:23,280
language models began they weren't

187
00:07:23,280 --> 00:07:25,199
specifically designed to do the tasks

188
00:07:25,199 --> 00:07:26,680
that we're using them for now they were

189
00:07:26,680 --> 00:07:28,319
designed as probabilistic models that

190
00:07:28,319 --> 00:07:31,080
are able to predict the next um the next

191
00:07:31,080 --> 00:07:34,199
token or word in a sentence and um in

192
00:07:34,199 --> 00:07:35,919
the early days we got these models as

193
00:07:35,919 --> 00:07:38,960
tools and um really there was a lot of

194
00:07:38,960 --> 00:07:41,080
trial and error to find techniques that

195
00:07:41,080 --> 00:07:44,000
worked well with them and um Ena them to

196
00:07:44,000 --> 00:07:46,599
you do useful things um so this led to

197
00:07:46,599 --> 00:07:48,520
things like Chain of Thought and F shop

198
00:07:48,520 --> 00:07:50,680
prompting adding personas things like

199
00:07:50,680 --> 00:07:52,919
that they they were just techniques that

200
00:07:52,919 --> 00:07:54,800
um were essentially discovered rather

201
00:07:54,800 --> 00:07:57,960
than designed um but in parallel we put

202
00:07:57,960 --> 00:08:00,759
a huge amount of work and effort into

203
00:08:00,759 --> 00:08:03,759
instruction tuning the models um uh so

204
00:08:03,759 --> 00:08:05,440
this is really us teaching the models

205
00:08:05,440 --> 00:08:07,919
how to behave in certain scenarios um

206
00:08:07,919 --> 00:08:10,319
this has progressed really rapidly um uh

207
00:08:10,319 --> 00:08:12,039
and it's moving to a future where like

208
00:08:12,039 --> 00:08:13,720
all the techniques are really designed

209
00:08:13,720 --> 00:08:16,039
techniques rather um and they're

210
00:08:16,039 --> 00:08:19,400
intentional um so as a team within

211
00:08:19,400 --> 00:08:22,080
Google it's it's our job to make llms as

212
00:08:22,080 --> 00:08:25,039
intuitive and easy to use as possible um

213
00:08:25,039 --> 00:08:26,800
and when I think about sort of prompt

214
00:08:26,800 --> 00:08:29,240
engineering I think of two sort of sets

215
00:08:29,240 --> 00:08:32,080
of Persona of user bases um you can

216
00:08:32,080 --> 00:08:34,959
think of end users um so those are folks

217
00:08:34,959 --> 00:08:36,719
maybe like using the Gemini app trying

218
00:08:36,719 --> 00:08:40,000
to use Gemini to answer questions um on

219
00:08:40,000 --> 00:08:41,760
a daily basis you know they may not be

220
00:08:41,760 --> 00:08:44,640
experts in prompting um and like really

221
00:08:44,640 --> 00:08:46,360
what we're trying to do there is get to

222
00:08:46,360 --> 00:08:48,839
a state where like no prompt engineering

223
00:08:48,839 --> 00:08:51,120
is required at all if um you should just

224
00:08:51,120 --> 00:08:52,839
be able to answer a user's reasonable

225
00:08:52,839 --> 00:08:55,320
request and um if there's something

226
00:08:55,320 --> 00:08:57,560
that's not clear then the app should um

227
00:08:57,560 --> 00:08:59,440
just be asking for clarification or

228
00:08:59,440 --> 00:09:01,079
offing multiple suggestions things like

229
00:09:01,079 --> 00:09:03,959
that um but then you can also think

230
00:09:03,959 --> 00:09:05,560
about people trying to build

231
00:09:05,560 --> 00:09:08,200
applications with other thems and um

232
00:09:08,200 --> 00:09:10,720
really what we're trying to do here is

233
00:09:10,720 --> 00:09:13,640
um make that process as simple and easy

234
00:09:13,640 --> 00:09:16,560
as possible like if Gemini um doesn't

235
00:09:16,560 --> 00:09:17,720
understand something in your prompt then

236
00:09:17,720 --> 00:09:19,519
it should be asking you about that um

237
00:09:19,519 --> 00:09:21,160
when you're developing your application

238
00:09:21,160 --> 00:09:23,519
rather than when you're deploying it um

239
00:09:23,519 --> 00:09:25,160
and really what what we're doing in

240
00:09:25,160 --> 00:09:26,360
parallel is kind of coming up with

241
00:09:26,360 --> 00:09:27,920
design patterns you know much the same

242
00:09:27,920 --> 00:09:30,040
way that programming language is evolved

243
00:09:30,040 --> 00:09:33,279
um and you got good design patterns for

244
00:09:33,279 --> 00:09:37,200
um like building applications um uh in

245
00:09:37,200 --> 00:09:38,640
like standard programming languages I

246
00:09:38,640 --> 00:09:40,680
see the same same thing happening in LM

247
00:09:40,680 --> 00:09:43,040
so you can imagine sort of guide books

248
00:09:43,040 --> 00:09:45,000
and things like that allowing you to

249
00:09:45,000 --> 00:09:48,279
sort of almost take off the shelf a um

250
00:09:48,279 --> 00:09:50,120
uh like an example bit of code and then

251
00:09:50,120 --> 00:09:52,160
customize that um to your specific

252
00:09:52,160 --> 00:09:54,640
application um when we talk about

253
00:09:54,640 --> 00:09:56,800
multimodal um I don't think anything

254
00:09:56,800 --> 00:09:58,120
should really be changing here in terms

255
00:09:58,120 --> 00:10:00,160
of our prompting techniques um you know

256
00:10:00,160 --> 00:10:01,200
one thing is that we're a little bit

257
00:10:01,200 --> 00:10:03,519
earlier in our journey um for multimodal

258
00:10:03,519 --> 00:10:07,200
prompts than um uh we are for text so

259
00:10:07,200 --> 00:10:09,120
like maybe we're still understanding

260
00:10:09,120 --> 00:10:11,600
where the gaps are um but I think it's

261
00:10:11,600 --> 00:10:13,760
actually really um really cool to try

262
00:10:13,760 --> 00:10:15,760
prompting um like the Gemini app by

263
00:10:15,760 --> 00:10:18,160
voice um because what you see there or

264
00:10:18,160 --> 00:10:20,240
certainly what I see is um a really

265
00:10:20,240 --> 00:10:23,360
impressive performance um despite the

266
00:10:23,360 --> 00:10:25,240
prompts really being less well written

267
00:10:25,240 --> 00:10:27,240
than they are in text um like if I'm

268
00:10:27,240 --> 00:10:28,680
talking to the Gemini app it'll be full

269
00:10:28,680 --> 00:10:29,880
of ums and

270
00:10:29,880 --> 00:10:31,320
and I might go back and correct my

271
00:10:31,320 --> 00:10:32,760
sentence you know I wouldn't do that if

272
00:10:32,760 --> 00:10:35,000
I was text prompting and yet what you

273
00:10:35,000 --> 00:10:39,120
really see is um like a very coherent um

274
00:10:39,120 --> 00:10:43,920
fluent process um excellent I I love the

275
00:10:43,920 --> 00:10:47,320
I love the the recommendation or the the

276
00:10:47,320 --> 00:10:49,240
the sort of forecast that in the future

277
00:10:49,240 --> 00:10:51,320
models will be asking for clarifying

278
00:10:51,320 --> 00:10:53,680
questions or or they'll be pulling in

279
00:10:53,680 --> 00:10:56,920
additional context to help support users

280
00:10:56,920 --> 00:10:59,360
requests um and make sure that they have

281
00:10:59,360 --> 00:11:01,760
the best possible outputs so it sounds

282
00:11:01,760 --> 00:11:03,519
it sounds like a Brave New World very

283
00:11:03,519 --> 00:11:07,240
excited for it in the future excellent

284
00:11:07,240 --> 00:11:10,040
um next question uh is all about vertex

285
00:11:10,040 --> 00:11:13,360
AI um so vertex AI is rapidly evolving

286
00:11:13,360 --> 00:11:15,639
with new features and capabilities

287
00:11:15,639 --> 00:11:17,200
looking ahead what are some of the key

288
00:11:17,200 --> 00:11:19,480
emerging Trends in Enterprise AI that

289
00:11:19,480 --> 00:11:21,240
you're most excited about and how is

290
00:11:21,240 --> 00:11:23,519
vertex AI positioned to help businesses

291
00:11:23,519 --> 00:11:26,480
leverage those for real world impact um

292
00:11:26,480 --> 00:11:28,639
Warren and Arena uh do you want to do

293
00:11:28,639 --> 00:11:30,959
you want to answer

294
00:11:30,959 --> 00:11:33,480
yeah sure um I'll go first Serena feel

295
00:11:33,480 --> 00:11:36,440
free to fill in um I think that when I

296
00:11:36,440 --> 00:11:38,360
look at like where we were and where

297
00:11:38,360 --> 00:11:41,160
we're going now um talking to customers

298
00:11:41,160 --> 00:11:43,079
we're in this kind of large place of

299
00:11:43,079 --> 00:11:44,800
business you know process automation

300
00:11:44,800 --> 00:11:46,399
where it was how do I understand

301
00:11:46,399 --> 00:11:48,160
unstructured data how do I pull it out

302
00:11:48,160 --> 00:11:49,920
and do things with it you know what

303
00:11:49,920 --> 00:11:51,839
we're seeing now as playing with the

304
00:11:51,839 --> 00:11:54,000
gentic Frameworks and some latest models

305
00:11:54,000 --> 00:11:56,399
last week is moving to this place of

306
00:11:56,399 --> 00:11:59,560
being able to uh understand and reason

307
00:11:59,560 --> 00:12:02,200
to kind of do deep research type things

308
00:12:02,200 --> 00:12:05,079
so Mar Way Beyond I just want to take

309
00:12:05,079 --> 00:12:06,680
this unstructured data and understand

310
00:12:06,680 --> 00:12:09,079
what it is to hey can I do comparative

311
00:12:09,079 --> 00:12:11,079
analysis of things and so when I was

312
00:12:11,079 --> 00:12:12,839
playing with the agent the model

313
00:12:12,839 --> 00:12:14,760
actually was smart enough to know that

314
00:12:14,760 --> 00:12:16,720
it didn't have the latest information

315
00:12:16,720 --> 00:12:18,959
and invoked a tool to go out actually on

316
00:12:18,959 --> 00:12:21,120
the web and find the latest information

317
00:12:21,120 --> 00:12:23,040
and bring it into the analysis I was

318
00:12:23,040 --> 00:12:26,880
doing and so it becomes much uh easier

319
00:12:26,880 --> 00:12:28,680
for you to do kind of some of this deep

320
00:12:28,680 --> 00:12:31,199
uh analys is and understanding of the

321
00:12:31,199 --> 00:12:33,240
data in the world and so I think that

322
00:12:33,240 --> 00:12:35,279
that's I see a ton of that in

323
00:12:35,279 --> 00:12:37,199
Enterprises going on where they're

324
00:12:37,199 --> 00:12:39,560
really getting Beyond just being able to

325
00:12:39,560 --> 00:12:41,279
search and understand that they've got a

326
00:12:41,279 --> 00:12:43,079
bunch of unstructured data and what to

327
00:12:43,079 --> 00:12:47,120
do with it Arena you want to fill

328
00:12:47,120 --> 00:12:50,399
in I think that sounds good

329
00:12:50,399 --> 00:12:54,120
great excellent and I I know that there

330
00:12:54,120 --> 00:12:56,760
uh the the question around evals and how

331
00:12:56,760 --> 00:12:59,320
to adequately evaluate these these

332
00:12:59,320 --> 00:13:01,760
agentic workflows is is something that

333
00:13:01,760 --> 00:13:03,639
uh that many companies are are thinking

334
00:13:03,639 --> 00:13:06,959
about and and starting to Pioneer um so

335
00:13:06,959 --> 00:13:09,920
I excited to hear more about uh Arena's

336
00:13:09,920 --> 00:13:14,959
uh uh work in evals later on as well um

337
00:13:14,959 --> 00:13:17,800
cool so next question is for everyone on

338
00:13:17,800 --> 00:13:20,800
the call um uh looking ahead one to

339
00:13:20,800 --> 00:13:23,360
three years what specific task or

340
00:13:23,360 --> 00:13:25,240
capability do you believe foundational

341
00:13:25,240 --> 00:13:26,880
models will unlock that seems

342
00:13:26,880 --> 00:13:29,560
challenging or impossible today um

343
00:13:29,560 --> 00:13:32,120
conversely what inherent limitations do

344
00:13:32,120 --> 00:13:33,920
you think will persist despite all of

345
00:13:33,920 --> 00:13:36,399
the progress that we've made um over the

346
00:13:36,399 --> 00:13:37,959
last couple of years and especially in

347
00:13:37,959 --> 00:13:41,079
the last several months so so just uh

348
00:13:41,079 --> 00:13:42,480
given that we have a lot of folks on the

349
00:13:42,480 --> 00:13:45,600
call let's keep it brief so around uh

350
00:13:45,600 --> 00:13:48,480
just two to three sentences um and to

351
00:13:48,480 --> 00:13:52,199
start U Matt do you want to go first

352
00:13:52,199 --> 00:13:55,320
sure three years in AI is 100 years in

353
00:13:55,320 --> 00:13:58,759
in human life so like that's question uh

354
00:13:58,759 --> 00:14:01,120
I think think the way we build software

355
00:14:01,120 --> 00:14:03,639
and the way we use software will

356
00:14:03,639 --> 00:14:05,600
radically change like change in ways

357
00:14:05,600 --> 00:14:07,560
that people are still not realizing I

358
00:14:07,560 --> 00:14:10,440
would summarize as that

359
00:14:10,440 --> 00:14:13,199
yeah and Logan what about you what do

360
00:14:13,199 --> 00:14:14,959
you think will be different in the next

361
00:14:14,959 --> 00:14:16,519
one to three

362
00:14:16,519 --> 00:14:19,120
years yeah I think the whole code

363
00:14:19,120 --> 00:14:21,120
generation software engineering stuff is

364
00:14:21,120 --> 00:14:22,519
going to continue to take off but I

365
00:14:22,519 --> 00:14:25,000
think the thing that is most interesting

366
00:14:25,000 --> 00:14:27,279
to me is I think on the context of

367
00:14:27,279 --> 00:14:29,920
what's not going to happen I do think

368
00:14:29,920 --> 00:14:32,880
the models are still going to be bad if

369
00:14:32,880 --> 00:14:34,800
you don't give them enough context like

370
00:14:34,800 --> 00:14:36,320
I feel like this is like not going to be

371
00:14:36,320 --> 00:14:38,600
a solved problem if you just like ask a

372
00:14:38,600 --> 00:14:40,079
really basic question and expect the

373
00:14:40,079 --> 00:14:41,880
model to be able to do some miraculous

374
00:14:41,880 --> 00:14:44,000
thing for you um I think you're you're

375
00:14:44,000 --> 00:14:45,360
still going to be disappointed in a few

376
00:14:45,360 --> 00:14:46,519
years maybe the models will be smart

377
00:14:46,519 --> 00:14:48,519
enough to know that they have to ask a

378
00:14:48,519 --> 00:14:49,560
bunch of follow-up questions or

379
00:14:49,560 --> 00:14:51,040
something like that in in the next one

380
00:14:51,040 --> 00:14:54,279
to three years but uh that that piece is

381
00:14:54,279 --> 00:14:56,079
is still going to

382
00:14:56,079 --> 00:14:59,040
persist absolutely the it's just like

383
00:14:59,040 --> 00:15:01,680
today if you ask a person to to solve a

384
00:15:01,680 --> 00:15:03,880
task or to or to do something for you

385
00:15:03,880 --> 00:15:06,040
you still need to give them enough uh

386
00:15:06,040 --> 00:15:07,759
enough background information to be

387
00:15:07,759 --> 00:15:09,320
successful and to point them in the

388
00:15:09,320 --> 00:15:10,399
right

389
00:15:10,399 --> 00:15:14,320
direction Arena do you want to go

390
00:15:14,320 --> 00:15:16,880
next I think mine is kind of similar

391
00:15:16,880 --> 00:15:19,120
from from the eval lens I think we will

392
00:15:19,120 --> 00:15:21,240
see less issues with how to automate

393
00:15:21,240 --> 00:15:23,959
eval flows but we will still be at the

394
00:15:23,959 --> 00:15:27,279
point where if you don't give the model

395
00:15:27,279 --> 00:15:29,279
your criteria and what you care of about

396
00:15:29,279 --> 00:15:31,160
and what you define is good there is

397
00:15:31,160 --> 00:15:33,279
just no way to to know that and that can

398
00:15:33,279 --> 00:15:35,360
be provided in context or somewhere else

399
00:15:35,360 --> 00:15:38,519
but you will still need to provide that

400
00:15:38,519 --> 00:15:41,920
somehow absolutely and

401
00:15:41,920 --> 00:15:43,759
Karen I might bring it back to the

402
00:15:43,759 --> 00:15:45,639
previous question and say that in a few

403
00:15:45,639 --> 00:15:47,079
years I hope that prompt engineering

404
00:15:47,079 --> 00:15:48,959
will be a thing of the past and I and i'

405
00:15:48,959 --> 00:15:51,560
expect it to be um uh But like everyone

406
00:15:51,560 --> 00:15:53,399
else says the models will never be able

407
00:15:53,399 --> 00:15:56,839
to read your mind and um uh people have

408
00:15:56,839 --> 00:15:59,040
to have to get more into the mindset

409
00:15:59,040 --> 00:16:02,560
being super clear and specific on their

410
00:16:02,560 --> 00:16:04,560
intention yeah and

411
00:16:04,560 --> 00:16:07,120
Warren I think even in this exists today

412
00:16:07,120 --> 00:16:09,600
but I think it gets worse is over time

413
00:16:09,600 --> 00:16:12,040
which is uh Enterprises especially are

414
00:16:12,040 --> 00:16:14,480
not built around the ability to move

415
00:16:14,480 --> 00:16:16,560
super quickly and so anything that

416
00:16:16,560 --> 00:16:18,240
happened six months ago that was two

417
00:16:18,240 --> 00:16:20,360
generations ago and so the ability for

418
00:16:20,360 --> 00:16:22,560
you to keep up and make sure that you

419
00:16:22,560 --> 00:16:24,440
design your you know the way that you

420
00:16:24,440 --> 00:16:26,920
roll out software the way that you put

421
00:16:26,920 --> 00:16:28,639
it in production that you can actually

422
00:16:28,639 --> 00:16:30,440
do that in an agile way that allows you

423
00:16:30,440 --> 00:16:32,680
to take the latest and greatest I think

424
00:16:32,680 --> 00:16:35,880
that that's uh one of the big uh issues

425
00:16:35,880 --> 00:16:37,920
that folks are are facing now and will

426
00:16:37,920 --> 00:16:40,079
continue to face as we move forward

427
00:16:40,079 --> 00:16:43,519
excellent and H and thank you so much to

428
00:16:43,519 --> 00:16:46,000
to everyone who's dialed in this week to

429
00:16:46,000 --> 00:16:48,560
to learn more about what's being built

430
00:16:48,560 --> 00:16:50,680
and to learn how to incorporate it into

431
00:16:50,680 --> 00:16:52,480
your businesses into your work or into

432
00:16:52,480 --> 00:16:54,279
your personal projects that is one of

433
00:16:54,279 --> 00:16:56,600
the first steps that you can do um to

434
00:16:56,600 --> 00:16:58,279
make sure that you're staying up to date

435
00:16:58,279 --> 00:17:00,000
and that as all of these great new

436
00:17:00,000 --> 00:17:02,000
features get released you are on top of

437
00:17:02,000 --> 00:17:04,919
all of them so so um good work to

438
00:17:04,919 --> 00:17:06,959
everybody dialed in today and learning

439
00:17:06,959 --> 00:17:09,280
more through the kaggle generative AI

440
00:17:09,280 --> 00:17:12,400
intensive course um the next question

441
00:17:12,400 --> 00:17:14,319
that we have is our first Community

442
00:17:14,319 --> 00:17:17,679
question um from donna. oie uh thank you

443
00:17:17,679 --> 00:17:20,600
for adding this on Discord how can AI

444
00:17:20,600 --> 00:17:22,959
system design and prompt engineering be

445
00:17:22,959 --> 00:17:25,600
optimized to improve Energy Efficiency

446
00:17:25,600 --> 00:17:27,720
computational performance so things like

447
00:17:27,720 --> 00:17:29,960
speed and accuracy and reduce

448
00:17:29,960 --> 00:17:32,080
environmental impact while maintaining

449
00:17:32,080 --> 00:17:35,120
output model quality um so Logan would

450
00:17:35,120 --> 00:17:37,480
you like to to take a stab at this

451
00:17:37,480 --> 00:17:39,480
one yeah this is a this is an

452
00:17:39,480 --> 00:17:40,840
interesting question I think there's a

453
00:17:40,840 --> 00:17:42,240
bunch of different dimensions I think

454
00:17:42,240 --> 00:17:44,080
one of them is

455
00:17:44,080 --> 00:17:46,720
um at some layer like different API

456
00:17:46,720 --> 00:17:48,360
Services have ways to help with this

457
00:17:48,360 --> 00:17:50,120
like you could do prompt caching as an

458
00:17:50,120 --> 00:17:53,160
example um I think there's also like you

459
00:17:53,160 --> 00:17:55,600
know another angle of this is like batch

460
00:17:55,600 --> 00:17:57,679
apis like you can take sort of you know

461
00:17:57,679 --> 00:18:00,720
the fixed cost of the fixed requirements

462
00:18:00,720 --> 00:18:02,840
of of having Services just like running

463
00:18:02,840 --> 00:18:04,799
all the time and find times when there's

464
00:18:04,799 --> 00:18:06,559
like idle compute just sitting around

465
00:18:06,559 --> 00:18:08,679
there um and be able to sort of flatten

466
00:18:08,679 --> 00:18:11,559
out and make sure that um you know the

467
00:18:11,559 --> 00:18:13,039
compu is being used from the Energy

468
00:18:13,039 --> 00:18:14,400
Efficiency standpoint you could imagine

469
00:18:14,400 --> 00:18:17,039
a world where like you say in the future

470
00:18:17,039 --> 00:18:18,760
this doesn't exist yet but you could say

471
00:18:18,760 --> 00:18:21,120
I'm a batch API customer and I care a

472
00:18:21,120 --> 00:18:23,000
lot about the environmental impact so

473
00:18:23,000 --> 00:18:25,360
actually try to run my batches times

474
00:18:25,360 --> 00:18:26,799
when you know data centers are more

475
00:18:26,799 --> 00:18:28,480
likely to be using renewable energy or

476
00:18:28,480 --> 00:18:30,159
something like that so I think there's a

477
00:18:30,159 --> 00:18:33,600
lot of degrees of freedom um and and

478
00:18:33,600 --> 00:18:35,159
dimensions in which in which you could

479
00:18:35,159 --> 00:18:38,000
do this absolutely and I know that you

480
00:18:38,000 --> 00:18:40,120
know Google's been investing a lot in in

481
00:18:40,120 --> 00:18:42,360
smaller models especially smaller open

482
00:18:42,360 --> 00:18:44,919
models and that can help reduce the the

483
00:18:44,919 --> 00:18:47,520
environmental impact footprint as well

484
00:18:47,520 --> 00:18:49,440
um if you're using something that's on

485
00:18:49,440 --> 00:18:52,240
device as opposed to to pinging a server

486
00:18:52,240 --> 00:18:54,840
with a larger model so it's it's been

487
00:18:54,840 --> 00:18:56,840
it's been really inspiring to see the

488
00:18:56,840 --> 00:18:59,120
creative ways that the community is kind

489
00:18:59,120 --> 00:19:01,159
of rallying around and and making these

490
00:19:01,159 --> 00:19:04,159
workloads more efficient in real

491
00:19:04,159 --> 00:19:07,480
time next question um this is from

492
00:19:07,480 --> 00:19:10,799
Channing Ogden um again from Discord how

493
00:19:10,799 --> 00:19:12,799
can judge models be selected and

494
00:19:12,799 --> 00:19:14,760
customized efficiently to minimize

495
00:19:14,760 --> 00:19:17,360
compounded bias and accuracy issues

496
00:19:17,360 --> 00:19:19,159
building confidence without relying

497
00:19:19,159 --> 00:19:22,520
solely on repeated evals um Arena do you

498
00:19:22,520 --> 00:19:25,320
want to take this one yes that's a great

499
00:19:25,320 --> 00:19:26,799
question and something I'm thinking

500
00:19:26,799 --> 00:19:29,080
about a lot how do you actually build

501
00:19:29,080 --> 00:19:31,159
trust in all the judge models and auto

502
00:19:31,159 --> 00:19:33,559
writers that you use so I I kind of

503
00:19:33,559 --> 00:19:35,880
think about three areas here first you

504
00:19:35,880 --> 00:19:37,679
just need to have a good foundation

505
00:19:37,679 --> 00:19:39,440
right so do I use a state-of-the-art

506
00:19:39,440 --> 00:19:42,080
model as a judge and do I have some core

507
00:19:42,080 --> 00:19:44,760
techniques in place to mitigate bias so

508
00:19:44,760 --> 00:19:46,200
just a couple examples you already

509
00:19:46,200 --> 00:19:47,960
mentioned multi sampling right so not

510
00:19:47,960 --> 00:19:49,880
relying on the first answer and there's

511
00:19:49,880 --> 00:19:52,000
other things like flipping because you

512
00:19:52,000 --> 00:19:54,320
need to flip orders as these models show

513
00:19:54,320 --> 00:19:56,200
a position bias they prefer the first or

514
00:19:56,200 --> 00:19:58,880
the second in a p w comparison so this

515
00:19:58,880 --> 00:20:02,159
would be kind of the first step and then

516
00:20:02,159 --> 00:20:04,440
I would say evaluate your judge it's yet

517
00:20:04,440 --> 00:20:06,280
another llm application so you want to

518
00:20:06,280 --> 00:20:07,679
test it and this doesn't have to be a

519
00:20:07,679 --> 00:20:10,720
lot of data but some basic understanding

520
00:20:10,720 --> 00:20:13,200
if the alignment if there is alignment

521
00:20:13,200 --> 00:20:15,000
between your human experts or your own

522
00:20:15,000 --> 00:20:18,280
judgment and what the judge says on

523
00:20:18,280 --> 00:20:20,559
again your very specific data and if you

524
00:20:20,559 --> 00:20:22,400
don't see that alignment and this is the

525
00:20:22,400 --> 00:20:25,039
third thing start with prompt

526
00:20:25,039 --> 00:20:26,840
engineering right we already spoke about

527
00:20:26,840 --> 00:20:29,679
this a lot today but are the criteria

528
00:20:29,679 --> 00:20:31,240
that you give the judge clear and

529
00:20:31,240 --> 00:20:34,120
specific I often see hidden criteria so

530
00:20:34,120 --> 00:20:36,799
users implicitly consider something but

531
00:20:36,799 --> 00:20:38,679
they don't really explicitly state it in

532
00:20:38,679 --> 00:20:41,000
the autter rator promt and as Kieran

533
00:20:41,000 --> 00:20:43,320
said maybe in the future they can ask

534
00:20:43,320 --> 00:20:45,240
clarifying questions but they don't do

535
00:20:45,240 --> 00:20:47,960
that today so this is something you have

536
00:20:47,960 --> 00:20:49,720
to think about and then after you've

537
00:20:49,720 --> 00:20:52,080
done this there's and and you see that

538
00:20:52,080 --> 00:20:53,919
refining The Prompt doesn't really close

539
00:20:53,919 --> 00:20:55,559
the alignment gap between you and the

540
00:20:55,559 --> 00:20:57,480
judge then you can explore more Advanced

541
00:20:57,480 --> 00:20:59,720
Techniques so maybe maybe the data set

542
00:20:59,720 --> 00:21:01,919
level criteria that you're working with

543
00:21:01,919 --> 00:21:03,520
they just don't fit your data set it's

544
00:21:03,520 --> 00:21:05,640
too diverse so maybe you need something

545
00:21:05,640 --> 00:21:07,400
like per item rubrics instead of

546
00:21:07,400 --> 00:21:09,919
universal criteria potentially you might

547
00:21:09,919 --> 00:21:11,559
consider fine-tuning your judge because

548
00:21:11,559 --> 00:21:14,000
your data set is so so specific but

549
00:21:14,000 --> 00:21:15,440
again I would start with the prompt

550
00:21:15,440 --> 00:21:17,120
engineering if you see some misalignment

551
00:21:17,120 --> 00:21:19,039
between you and the judge model

552
00:21:19,039 --> 00:21:20,640
excellent I feel like we all just got a

553
00:21:20,640 --> 00:21:23,919
crash course in uh in evaluating and

554
00:21:23,919 --> 00:21:25,960
sort of perfecting judge models this is

555
00:21:25,960 --> 00:21:28,240
wonderful um and I hope we I hope we get

556
00:21:28,240 --> 00:21:29,720
to cover for a little bit more of it

557
00:21:29,720 --> 00:21:34,640
later on in the week cool um next

558
00:21:34,640 --> 00:21:38,840
question um from sarar 42 uh is writing

559
00:21:38,840 --> 00:21:41,000
the prompt appropriately prompt

560
00:21:41,000 --> 00:21:42,960
engineering or setting up the number of

561
00:21:42,960 --> 00:21:45,120
tokens temperature top p is prompt

562
00:21:45,120 --> 00:21:48,840
engineering or both um and uh an not do

563
00:21:48,840 --> 00:21:50,200
you want to do you want to take a stab

564
00:21:50,200 --> 00:21:52,640
at answering this question um I also

565
00:21:52,640 --> 00:21:55,520
love to hear everyone's uh everyone's

566
00:21:55,520 --> 00:21:57,320
initial thoughts around prompt

567
00:21:57,320 --> 00:21:59,600
engineering what is it why is it useful

568
00:21:59,600 --> 00:22:02,159
and what exactly um what exactly does it

569
00:22:02,159 --> 00:22:05,080
entail so maybe I just give a quick uh

570
00:22:05,080 --> 00:22:06,880
overview and then uh the rest can take

571
00:22:06,880 --> 00:22:09,480
over so I see prompt The Prompt part of

572
00:22:09,480 --> 00:22:11,240
the prompt engineering as the input like

573
00:22:11,240 --> 00:22:12,840
in traditional ml models where there

574
00:22:12,840 --> 00:22:15,279
were features so prompt is the input to

575
00:22:15,279 --> 00:22:18,320
the model while the the other parameters

576
00:22:18,320 --> 00:22:20,159
the generation or decoding parameters

577
00:22:20,159 --> 00:22:22,400
like top PE temperature these are

578
00:22:22,400 --> 00:22:24,520
operating at the output level where we

579
00:22:24,520 --> 00:22:27,360
kind of uh with the fixed input what

580
00:22:27,360 --> 00:22:29,360
else we can modify the the output to

581
00:22:29,360 --> 00:22:30,960
kind of ensure that the tokens that are

582
00:22:30,960 --> 00:22:34,520
selected and sampled are um done so in a

583
00:22:34,520 --> 00:22:37,400
way that optimizes the response for the

584
00:22:37,400 --> 00:22:40,400
task anybody else uh want to take a step

585
00:22:40,400 --> 00:22:44,720
at this maybe um uh Matt or

586
00:22:44,720 --> 00:22:46,279
airon

587
00:22:46,279 --> 00:22:49,440
sure I'll ask K to cover his ears as I

588
00:22:49,440 --> 00:22:51,520
say this but like my opinion is propt

589
00:22:51,520 --> 00:22:53,880
engineer is a little bit of an art right

590
00:22:53,880 --> 00:22:55,559
it's a little bit of try and error it's

591
00:22:55,559 --> 00:22:58,000
a little bit of let me test this with

592
00:22:58,000 --> 00:23:00,360
multiple models let me test this with

593
00:23:00,360 --> 00:23:02,840
multiple temperature settings does a

594
00:23:02,840 --> 00:23:05,159
smaller model can do this job or do I

595
00:23:05,159 --> 00:23:07,360
need a larger model like a lot of these

596
00:23:07,360 --> 00:23:09,120
things I put in the bucket of prompt

597
00:23:09,120 --> 00:23:11,320
engineering which is experimentation

598
00:23:11,320 --> 00:23:14,279
over and over again until you find the

599
00:23:14,279 --> 00:23:17,279
optimal uh you know way of working for

600
00:23:17,279 --> 00:23:19,520
your

601
00:23:20,039 --> 00:23:22,520
scenario and yeah I I'd agree I'd agree

602
00:23:22,520 --> 00:23:24,799
with the art points at the minute um

603
00:23:24,799 --> 00:23:26,760
like I see a future where there's far

604
00:23:26,760 --> 00:23:28,960
less art involved and

605
00:23:28,960 --> 00:23:30,799
you know if we think about this sort of

606
00:23:30,799 --> 00:23:32,120
specific question you know whether you

607
00:23:32,120 --> 00:23:34,279
call it prompt engineering or llm

608
00:23:34,279 --> 00:23:35,840
engineering or whatever these are all

609
00:23:35,840 --> 00:23:37,679
things as a developer that you have to

610
00:23:37,679 --> 00:23:40,480
think about um and there are various

611
00:23:40,480 --> 00:23:43,360
knobs that you can control um and you

612
00:23:43,360 --> 00:23:45,640
may not you need to play with them a bit

613
00:23:45,640 --> 00:23:47,360
to build up an appreciation of the

614
00:23:47,360 --> 00:23:49,640
effects that they're going to have um

615
00:23:49,640 --> 00:23:51,440
and there's something that I would

616
00:23:51,440 --> 00:23:54,720
expect the um like need to go down for

617
00:23:54,720 --> 00:23:56,400
in the future as well like temperature

618
00:23:56,400 --> 00:23:58,880
is really just a way of balancing your

619
00:23:58,880 --> 00:24:02,000
creativity um and uh like increasing

620
00:24:02,000 --> 00:24:03,919
your creativity to make sure you don't

621
00:24:03,919 --> 00:24:07,559
get the same response every time um and

622
00:24:07,559 --> 00:24:10,279
uh that's uh that's I guess a knob that

623
00:24:10,279 --> 00:24:14,679
we expect to sort of to stay um but um

624
00:24:14,679 --> 00:24:16,120
be clear on what these parameters are

625
00:24:16,120 --> 00:24:17,559
are doing and expect things to look a

626
00:24:17,559 --> 00:24:19,279
bit different in the future just one

627
00:24:19,279 --> 00:24:21,039
thing to add on to that for those of you

628
00:24:21,039 --> 00:24:22,720
who haven't read The Prompt engineering

629
00:24:22,720 --> 00:24:24,360
white paper yet we have a section on

630
00:24:24,360 --> 00:24:26,360
automated prompt engineering which kind

631
00:24:26,360 --> 00:24:28,159
of crafts a prompt uses together with

632
00:24:28,159 --> 00:24:30,760
the evaluation topic it evaluates and

633
00:24:30,760 --> 00:24:33,399
crafts it for you so have a look at that

634
00:24:33,399 --> 00:24:38,159
it's very useful um for your projects

635
00:24:38,159 --> 00:24:41,039
absolutely next question um

636
00:24:41,039 --> 00:24:43,200
Hallucination is a major challenge for

637
00:24:43,200 --> 00:24:45,240
large language models techniques like

638
00:24:45,240 --> 00:24:47,760
Rag and prompt engineering can help um

639
00:24:47,760 --> 00:24:49,880
but what are the most effective methods

640
00:24:49,880 --> 00:24:53,279
that Google uses in Gemini 2 to minimize

641
00:24:53,279 --> 00:24:55,399
uh incorrect or misleading outputs are

642
00:24:55,399 --> 00:24:57,159
there trade-offs between reducing

643
00:24:57,159 --> 00:25:00,320
hallucinations and model creativity um

644
00:25:00,320 --> 00:25:02,240
Kieran uh do you want to do you want to

645
00:25:02,240 --> 00:25:04,159
take a stab with this one sure

646
00:25:04,159 --> 00:25:07,200
absolutely so reducing hallucinations um

647
00:25:07,200 --> 00:25:08,440
or you know this is an area that we call

648
00:25:08,440 --> 00:25:10,399
factuality as well it's one of our key

649
00:25:10,399 --> 00:25:12,120
areas of focus it's one of the things

650
00:25:12,120 --> 00:25:14,840
that um was very apparent in LMS in the

651
00:25:14,840 --> 00:25:17,720
early days and um it's critical to make

652
00:25:17,720 --> 00:25:19,600
them like most useful going forwards and

653
00:25:19,600 --> 00:25:20,880
I think there has been a lot of progress

654
00:25:20,880 --> 00:25:23,840
over the last couple of years um uh when

655
00:25:23,840 --> 00:25:26,360
I think about H Nations I think of it in

656
00:25:26,360 --> 00:25:28,320
sort of terms of sort of two different

657
00:25:28,320 --> 00:25:31,720
framings um one is whether um Gemini is

658
00:25:31,720 --> 00:25:34,159
trying to answer a question or Pro

659
00:25:34,159 --> 00:25:36,080
provide an answer based on a bit of

660
00:25:36,080 --> 00:25:37,880
context that has been input um so you

661
00:25:37,880 --> 00:25:39,799
know that can be rag but it can also be

662
00:25:39,799 --> 00:25:41,640
like answering questions over documents

663
00:25:41,640 --> 00:25:45,159
that you provide um and also if you look

664
00:25:45,159 --> 00:25:47,520
at the um the generative experience in

665
00:25:47,520 --> 00:25:49,320
Google search that's what happens um

666
00:25:49,320 --> 00:25:50,919
like gini will go away and do a search

667
00:25:50,919 --> 00:25:53,399
and then uh of summarize those results

668
00:25:53,399 --> 00:25:55,919
for you so um it's able to produce its

669
00:25:55,919 --> 00:25:57,760
answer based entirely on knowledge that

670
00:25:57,760 --> 00:25:59,960
is being Prov ided to it um and then

671
00:25:59,960 --> 00:26:02,200
there's a second one which is where um

672
00:26:02,200 --> 00:26:05,039
Gemini is um like answering essentially

673
00:26:05,039 --> 00:26:07,640
from um from its training data or you

674
00:26:07,640 --> 00:26:09,600
know if you think of human analogy it's

675
00:26:09,600 --> 00:26:10,840
kind of like answering from your

676
00:26:10,840 --> 00:26:15,200
education or um your memory um the first

677
00:26:15,200 --> 00:26:17,960
is always going to be um like inherently

678
00:26:17,960 --> 00:26:20,679
a bit easier for it to do and um you

679
00:26:20,679 --> 00:26:22,520
know probably a safer bet you know I've

680
00:26:22,520 --> 00:26:24,640
I it's a lot easier for me to verify an

681
00:26:24,640 --> 00:26:26,159
answer if I'm looking at some Source

682
00:26:26,159 --> 00:26:27,880
materials in front of me than if I'm

683
00:26:27,880 --> 00:26:30,840
having to sort of troll through um some

684
00:26:30,840 --> 00:26:33,120
distant knowledge of facts In My Memory

685
00:26:33,120 --> 00:26:36,520
um so um really if you're trying to

686
00:26:36,520 --> 00:26:39,240
reduce hallucinations finding ways to

687
00:26:39,240 --> 00:26:42,080
ground to the input um is like a very

688
00:26:42,080 --> 00:26:43,799
good strategy and like vertex offer

689
00:26:43,799 --> 00:26:47,360
search grounding as um an option on the

690
00:26:47,360 --> 00:26:49,240
API um so what you're really doing there

691
00:26:49,240 --> 00:26:51,360
is giving verifiable um references to

692
00:26:51,360 --> 00:26:54,840
justify the answers is coming out um um

693
00:26:54,840 --> 00:26:57,760
beyond that um you know you can be uh

694
00:26:57,760 --> 00:26:59,760
explicit in your prompt about what your

695
00:26:59,760 --> 00:27:02,399
requirements here are that may help um

696
00:27:02,399 --> 00:27:04,039
and you can also add on explicit

697
00:27:04,039 --> 00:27:06,039
verification steps at the end if you

698
00:27:06,039 --> 00:27:09,480
want to be really uh really um like uh

699
00:27:09,480 --> 00:27:12,960
mindful about your factuality um uh llms

700
00:27:12,960 --> 00:27:15,039
are also very good at verifying answers

701
00:27:15,039 --> 00:27:16,600
and checking whether an answer coming

702
00:27:16,600 --> 00:27:19,799
back is uh meets a certain criteria so

703
00:27:19,799 --> 00:27:21,799
um you can try that strategy um even

704
00:27:21,799 --> 00:27:24,399
maybe combined with self-correction um

705
00:27:24,399 --> 00:27:26,279
to uh like go away and correct any

706
00:27:26,279 --> 00:27:29,640
errors that you see um and in terms of

707
00:27:29,640 --> 00:27:31,960
the balance between uh like factuality

708
00:27:31,960 --> 00:27:35,440
and creativity um you know there is a uh

709
00:27:35,440 --> 00:27:37,559
a trade-off there um you know it's

710
00:27:37,559 --> 00:27:40,320
difficult to write a very creative poem

711
00:27:40,320 --> 00:27:43,799
that is grounded in sort of real fact um

712
00:27:43,799 --> 00:27:46,399
um but uh you know something to be aware

713
00:27:46,399 --> 00:27:47,720
of coming back to the previous point

714
00:27:47,720 --> 00:27:49,720
about essentially the temperature knob

715
00:27:49,720 --> 00:27:52,320
um when you increase the temperature um

716
00:27:52,320 --> 00:27:55,159
what you're doing is you're making it um

717
00:27:55,159 --> 00:27:56,720
uh you're making it more likely for the

718
00:27:56,720 --> 00:27:59,360
model to pick a less probable token uh

719
00:27:59,360 --> 00:28:01,000
because these are probabilistic models

720
00:28:01,000 --> 00:28:04,120
um so when you're exploring your

721
00:28:04,120 --> 00:28:06,799
factuality you can play it safe and uh

722
00:28:06,799 --> 00:28:08,840
turn the temperature right down to zero

723
00:28:08,840 --> 00:28:11,159
and you can also look empirically at the

724
00:28:11,159 --> 00:28:12,600
results that you're getting back as you

725
00:28:12,600 --> 00:28:14,799
increase that to see what is the right

726
00:28:14,799 --> 00:28:16,600
balance for you in your use

727
00:28:16,600 --> 00:28:19,679
case absolutely just like uh Warren was

728
00:28:19,679 --> 00:28:21,600
mentioning a little bit earlier I love

729
00:28:21,600 --> 00:28:23,440
all of the knobs and dials that you can

730
00:28:23,440 --> 00:28:25,760
use to to ground and to reduce the

731
00:28:25,760 --> 00:28:27,679
likelihood of hallucinations for models

732
00:28:27,679 --> 00:28:30,120
things like search grounding or or code

733
00:28:30,120 --> 00:28:33,159
execution um these are all wonderful um

734
00:28:33,159 --> 00:28:35,559
wonderful methods for for getting the

735
00:28:35,559 --> 00:28:37,440
right kinds of outputs from from the

736
00:28:37,440 --> 00:28:39,960
models that we have available

737
00:28:39,960 --> 00:28:43,360
today and with that uh thank you so much

738
00:28:43,360 --> 00:28:46,000
to all of our expert guests uh for

739
00:28:46,000 --> 00:28:47,880
coming today for for getting to share a

740
00:28:47,880 --> 00:28:49,039
little bit more about what you're

741
00:28:49,039 --> 00:28:50,720
working on and to answer all of our

742
00:28:50,720 --> 00:28:52,880
great Community questions we really

743
00:28:52,880 --> 00:28:56,039
appreciate you and your time uh and am

744
00:28:56,039 --> 00:28:58,360
looking forward to seeing what uh what

745
00:28:58,360 --> 00:29:00,760
y'all um build and release over the

746
00:29:00,760 --> 00:29:02,399
course of the next several months this

747
00:29:02,399 --> 00:29:06,240
has been excellent thank

748
00:29:06,240 --> 00:29:10,480
you wonderful and now uh uh one of the

749
00:29:10,480 --> 00:29:14,120
most exciting parts of the of the the

750
00:29:14,120 --> 00:29:15,960
sort of kaggle generative AI intensive

751
00:29:15,960 --> 00:29:17,919
course at least to me I'm delighted to

752
00:29:17,919 --> 00:29:20,840
welcome on to the stage um anant who is

753
00:29:20,840 --> 00:29:23,440
going to be going over our code labs and

754
00:29:23,440 --> 00:29:26,640
demos um as well as giving a a brief

755
00:29:26,640 --> 00:29:28,600
overview of of some of the cont content

756
00:29:28,600 --> 00:29:29,760
that you all should have been learning

757
00:29:29,760 --> 00:29:31,600
about over the course of the last 24

758
00:29:31,600 --> 00:29:35,240
hours um take it away an a thanks paig

759
00:29:35,240 --> 00:29:39,120
so hi everyone um so uh we aware that uh

760
00:29:39,120 --> 00:29:40,559
some of you are directly joining for the

761
00:29:40,559 --> 00:29:42,600
live stream and uh I'm going to give you

762
00:29:42,600 --> 00:29:44,440
a quick overview of the white papers and

763
00:29:44,440 --> 00:29:46,159
then move on to the code labs to give

764
00:29:46,159 --> 00:29:48,080
you a flavor of what you learned or will

765
00:29:48,080 --> 00:29:50,080
learn if you have haven't had a chance

766
00:29:50,080 --> 00:29:53,799
to dive into it so uh uh let's start off

767
00:29:53,799 --> 00:29:56,559
with the white paper overview so the we

768
00:29:56,559 --> 00:29:58,440
had two white papers the found one on

769
00:29:58,440 --> 00:30:00,240
foundational models and the one on

770
00:30:00,240 --> 00:30:02,480
prompt engineering and first in the

771
00:30:02,480 --> 00:30:04,760
foundational model we looked at the uh

772
00:30:04,760 --> 00:30:07,240
basically how these AI models which

773
00:30:07,240 --> 00:30:09,279
often use a Transformer architecture

774
00:30:09,279 --> 00:30:11,240
leverage the attention mechanism to

775
00:30:11,240 --> 00:30:14,559
train on like large Corpus and leverage

776
00:30:14,559 --> 00:30:16,840
large context we also looked at

777
00:30:16,840 --> 00:30:18,919
architectural variations like mixture of

778
00:30:18,919 --> 00:30:20,919
experts how they can improve efficiency

779
00:30:20,919 --> 00:30:23,440
and quality we also saw the rapid

780
00:30:23,440 --> 00:30:25,200
Evolution through different models all

781
00:30:25,200 --> 00:30:28,240
the way from birt Palm to Gemini along

782
00:30:28,240 --> 00:30:30,760
with several open um models as well

783
00:30:30,760 --> 00:30:33,760
driven by scaling data and model size

784
00:30:33,760 --> 00:30:36,159
next we looked at how these models are

785
00:30:36,159 --> 00:30:38,919
trained and adapted so they start off

786
00:30:38,919 --> 00:30:41,360
with pre-training on v data sets for

787
00:30:41,360 --> 00:30:43,640
basically just building a general

788
00:30:43,640 --> 00:30:46,480
understanding of um the modality they're

789
00:30:46,480 --> 00:30:49,279
training on then often to ensure that

790
00:30:49,279 --> 00:30:51,279
they we looked at basically to ensure

791
00:30:51,279 --> 00:30:53,240
that they follow the instructions that

792
00:30:53,240 --> 00:30:55,840
you provide we use super they go through

793
00:30:55,840 --> 00:30:59,200
a supervised fine tuning state AG um uh

794
00:30:59,200 --> 00:31:01,360
to improve instruction following and to

795
00:31:01,360 --> 00:31:04,960
make them more task specific and lastly

796
00:31:04,960 --> 00:31:06,600
um we looked at how reinforcement

797
00:31:06,600 --> 00:31:08,880
learning from Human feedback also called

798
00:31:08,880 --> 00:31:11,880
rlf aligns the outputs with human

799
00:31:11,880 --> 00:31:14,600
preferences for basically things like uh

800
00:31:14,600 --> 00:31:17,559
helpfulness and safety then we looked at

801
00:31:17,559 --> 00:31:20,120
okay the training uh tuning these models

802
00:31:20,120 --> 00:31:22,799
especially to tasks um Downstream toss

803
00:31:22,799 --> 00:31:25,279
quite expensive so we can do we use

804
00:31:25,279 --> 00:31:27,720
various parameter efficient methods

805
00:31:27,720 --> 00:31:30,120
which which uh make uh tuning these uh

806
00:31:30,120 --> 00:31:32,760
models very efficient we all in the

807
00:31:32,760 --> 00:31:35,159
second paper on prompt engineering right

808
00:31:35,159 --> 00:31:36,720
um this is a core part of what we

809
00:31:36,720 --> 00:31:38,960
discussed in the earlier on in the Q&A

810
00:31:38,960 --> 00:31:40,679
session we looked at the various

811
00:31:40,679 --> 00:31:42,840
prompting techniques all the way from

812
00:31:42,840 --> 00:31:45,039
generation or sampling parameters such

813
00:31:45,039 --> 00:31:48,000
as temperature which controls the

814
00:31:48,000 --> 00:31:50,080
randomness uh and diversity of the

815
00:31:50,080 --> 00:31:53,320
output top p and top K and how it's

816
00:31:53,320 --> 00:31:55,919
crucial to balance predictability and

817
00:31:55,919 --> 00:31:58,480
creativ creativity depending on the task

818
00:31:58,480 --> 00:32:01,600
you are using them for we also looked at

819
00:32:01,600 --> 00:32:03,639
various prompting techniques all the way

820
00:32:03,639 --> 00:32:06,600
from uh basic zero shot techniques where

821
00:32:06,600 --> 00:32:08,880
you just ask the llm to providing

822
00:32:08,880 --> 00:32:12,000
examples to the llm uh uh to make it

823
00:32:12,000 --> 00:32:13,679
more effective for the tasks that you're

824
00:32:13,679 --> 00:32:15,760
using it for we also looked at

825
00:32:15,760 --> 00:32:18,000
structuring prompts uh or structuring

826
00:32:18,000 --> 00:32:20,600
prompts uh with system instructions task

827
00:32:20,600 --> 00:32:23,120
relevant context or assigning a role

828
00:32:23,120 --> 00:32:25,600
also can help guide the model and we

829
00:32:25,600 --> 00:32:28,519
also then um later on uh look at things

830
00:32:28,519 --> 00:32:30,360
like for more complex problems which

831
00:32:30,360 --> 00:32:32,279
involve reasoning Chain of Thought

832
00:32:32,279 --> 00:32:35,519
models uh step by prompting prompting

833
00:32:35,519 --> 00:32:37,440
and uh other techniques which can help

834
00:32:37,440 --> 00:32:40,080
with uh enhance complex problem solving

835
00:32:40,080 --> 00:32:43,200
for models finally uh in the

836
00:32:43,200 --> 00:32:46,039
foundational model chapter we looked at

837
00:32:46,039 --> 00:32:48,880
um uh how to optimize the models for

838
00:32:48,880 --> 00:32:50,919
Speed and efficiency as discussed

839
00:32:50,919 --> 00:32:52,840
earlier on in one of the Q&A questions

840
00:32:52,840 --> 00:32:54,639
there various techniques that we can use

841
00:32:54,639 --> 00:32:56,240
for that from

842
00:32:56,240 --> 00:32:58,440
quantization uh distill

843
00:32:58,440 --> 00:33:00,480
as well as various other techniques such

844
00:33:00,480 --> 00:33:02,840
as speculative decoding which basically

845
00:33:02,840 --> 00:33:05,799
makes models faster and cheaper I would

846
00:33:05,799 --> 00:33:08,039
recommend uh looking into the podcast of

847
00:33:08,039 --> 00:33:10,600
white paper to know more about them and

848
00:33:10,600 --> 00:33:13,240
then finally we concluded the whole um

849
00:33:13,240 --> 00:33:15,240
paper with looking at evaluation and

850
00:33:15,240 --> 00:33:17,080
best practices for evaluating your

851
00:33:17,080 --> 00:33:19,880
models using other llms as well as well

852
00:33:19,880 --> 00:33:24,080
as uh simpler techniques so yes um now

853
00:33:24,080 --> 00:33:25,919
that we have uh kind of gotten an

854
00:33:25,919 --> 00:33:28,639
overview of what we that in the reading

855
00:33:28,639 --> 00:33:31,880
assignments let us dive straight into

856
00:33:31,880 --> 00:33:33,559
I'm going to be sharing my screen for

857
00:33:33,559 --> 00:33:36,320
the code

858
00:33:40,840 --> 00:33:44,480
lab so hope everybody can see my screen

859
00:33:44,480 --> 00:33:47,720
so the first code lab um that you all

860
00:33:47,720 --> 00:33:51,080
have received basically dives into um

861
00:33:51,080 --> 00:33:53,000
prompt engineering and how we can

862
00:33:53,000 --> 00:33:57,279
utilize these um um models to for your

863
00:33:57,279 --> 00:34:00,240
uh applic ations so the first part of it

864
00:34:00,240 --> 00:34:03,440
is basically just using Gemini 2.0 flash

865
00:34:03,440 --> 00:34:06,480
which is one of our most uh performant

866
00:34:06,480 --> 00:34:09,320
um performance and speed balance models

867
00:34:09,320 --> 00:34:13,119
uh uh that uh we released and this uh we

868
00:34:13,119 --> 00:34:15,480
use it to see how we can do simple

869
00:34:15,480 --> 00:34:19,040
prompting here then uh we move on from

870
00:34:19,040 --> 00:34:21,200
this single turn prompting where we just

871
00:34:21,200 --> 00:34:24,000
give an input and get an output to a

872
00:34:24,000 --> 00:34:26,040
multi-term structure where we can have a

873
00:34:26,040 --> 00:34:29,320
conversation with the model and the the

874
00:34:29,320 --> 00:34:31,480
the the API automatically retains

875
00:34:31,480 --> 00:34:33,720
previous context to inform forther

876
00:34:33,720 --> 00:34:35,679
responses by the model for

877
00:34:35,679 --> 00:34:38,200
conversational applications and then we

878
00:34:38,200 --> 00:34:39,720
looked at the various option that you

879
00:34:39,720 --> 00:34:41,919
can uh of models that we can utilize

880
00:34:41,919 --> 00:34:45,560
from the API Beyond just 2.0 flash this

881
00:34:45,560 --> 00:34:48,919
uh we this this is um you can also use

882
00:34:48,919 --> 00:34:52,079
your own tuned models and uh they

883
00:34:52,079 --> 00:34:54,839
provide them as um like specify the

884
00:34:54,839 --> 00:34:58,320
model for your um API call

885
00:34:58,320 --> 00:35:01,520
and the the next part of the Cod lab

886
00:35:01,520 --> 00:35:03,720
which you'll be learning from here is um

887
00:35:03,720 --> 00:35:06,359
the how to like uh modify the various

888
00:35:06,359 --> 00:35:08,280
generation parameters and you'll be

889
00:35:08,280 --> 00:35:10,280
playing around with a lot some of them

890
00:35:10,280 --> 00:35:12,400
for instance output length this is

891
00:35:12,400 --> 00:35:15,000
basically um specifi telling the model

892
00:35:15,000 --> 00:35:17,560
to um like limit the amount of tokens

893
00:35:17,560 --> 00:35:20,280
it's generating it's a hard limit keep

894
00:35:20,280 --> 00:35:22,560
in mind so it does not automatically

895
00:35:22,560 --> 00:35:25,320
tell the model to automatically generate

896
00:35:25,320 --> 00:35:28,119
a smaller like a concise response it's

897
00:35:28,119 --> 00:35:30,320
essentially just truncates the response

898
00:35:30,320 --> 00:35:33,320
so if you are going to ask the model to

899
00:35:33,320 --> 00:35:35,320
make like a thousand-word essay and give

900
00:35:35,320 --> 00:35:38,839
it a very short like response like uh

901
00:35:38,839 --> 00:35:40,680
Max response length it's going to just

902
00:35:40,680 --> 00:35:43,320
cut off the essay abruptly so keep that

903
00:35:43,320 --> 00:35:45,240
in mind uh but it can help you control

904
00:35:45,240 --> 00:35:47,359
costs then we looked at something we

905
00:35:47,359 --> 00:35:48,920
have talked about earlier what Kiran

906
00:35:48,920 --> 00:35:50,920
mentioned earlier temperature this

907
00:35:50,920 --> 00:35:52,480
basically controls the degree of

908
00:35:52,480 --> 00:35:55,319
Randomness in token selection and long

909
00:35:55,319 --> 00:35:57,359
story short um a higher temperature

910
00:35:57,359 --> 00:35:59,240
leads Le to more diverse outputs while a

911
00:35:59,240 --> 00:36:00,480
lower temperature leads to more

912
00:36:00,480 --> 00:36:02,800
predictable deterministic outputs we

913
00:36:02,800 --> 00:36:05,040
looked at an example of how when asking

914
00:36:05,040 --> 00:36:07,760
the model to pick a color a random color

915
00:36:07,760 --> 00:36:10,800
it can pick different colors um across

916
00:36:10,800 --> 00:36:12,599
different iterations uh when their

917
00:36:12,599 --> 00:36:14,520
temperature is higher while for a lower

918
00:36:14,520 --> 00:36:16,680
temperature it tends to center around

919
00:36:16,680 --> 00:36:17,920
one single

920
00:36:17,920 --> 00:36:20,160
color then we also looked at things like

921
00:36:20,160 --> 00:36:21,920
top how we can play around with knobs

922
00:36:21,920 --> 00:36:24,319
like top p and top K which also kind of

923
00:36:24,319 --> 00:36:26,680
constrain the tokens that the model

924
00:36:26,680 --> 00:36:28,960
selects at the coding time or generation

925
00:36:28,960 --> 00:36:32,480
time this can help you uh with your um

926
00:36:32,480 --> 00:36:34,000
uh with selecting the amount of

927
00:36:34,000 --> 00:36:36,720
Randomness and determinism in your

928
00:36:36,720 --> 00:36:39,359
applications and then towards the last

929
00:36:39,359 --> 00:36:41,280
section of the first C laab we looked at

930
00:36:41,280 --> 00:36:43,440
various uh prompting techniques that we

931
00:36:43,440 --> 00:36:45,440
have discussed earlier zero shot where

932
00:36:45,440 --> 00:36:47,359
we give it a prompt and give it a task

933
00:36:47,359 --> 00:36:50,960
and ask a response all the way to um

934
00:36:50,960 --> 00:36:54,400
using like constraining the response so

935
00:36:54,400 --> 00:36:56,640
instead of a free text field where we

936
00:36:56,640 --> 00:36:59,760
just ask the model to generate some uh

937
00:36:59,760 --> 00:37:02,040
text uh without the constraints we can

938
00:37:02,040 --> 00:37:03,760
also kind of limit the responses that

939
00:37:03,760 --> 00:37:06,359
the model can provide us the enumeration

940
00:37:06,359 --> 00:37:09,400
enumeration set and we looked at also

941
00:37:09,400 --> 00:37:11,359
other techniques like one shot and few

942
00:37:11,359 --> 00:37:12,960
shot where we provide some input and

943
00:37:12,960 --> 00:37:15,079
output examples to help it perform

944
00:37:15,079 --> 00:37:18,000
better on certain tasks and um things

945
00:37:18,000 --> 00:37:20,720
like Json mode uh where we can structure

946
00:37:20,720 --> 00:37:23,440
give it a certain the provide the model

947
00:37:23,440 --> 00:37:26,000
to a certain structure for its output it

948
00:37:26,000 --> 00:37:28,720
can help it um uh structure its output

949
00:37:28,720 --> 00:37:30,800
in a way which can easily be parsed by

950
00:37:30,800 --> 00:37:33,280
the downstream models and then Chain of

951
00:37:33,280 --> 00:37:35,359
Thought reasoning um and other prompting

952
00:37:35,359 --> 00:37:36,839
techniques as

953
00:37:36,839 --> 00:37:40,200
well and react as well so that was the

954
00:37:40,200 --> 00:37:42,760
first collab and moving on to the second

955
00:37:42,760 --> 00:37:45,599
collab which is also um we doing it for

956
00:37:45,599 --> 00:37:48,440
first time this year um is the one on

957
00:37:48,440 --> 00:37:51,079
evaluation and structured output so it's

958
00:37:51,079 --> 00:37:53,440
as we learned in the podcast in our

959
00:37:53,440 --> 00:37:55,440
discussion earlier evaluating the respon

960
00:37:55,440 --> 00:37:58,000
uh response is pretty crucial especially

961
00:37:58,000 --> 00:38:02,079
for your tasks and um we look in uh in

962
00:38:02,079 --> 00:38:05,240
this code lab we we look at how you can

963
00:38:05,240 --> 00:38:08,960
um basically um set up um set up some

964
00:38:08,960 --> 00:38:12,040
context as like a PDF um for one of our

965
00:38:12,040 --> 00:38:16,720
technical reports and utilize um uh an

966
00:38:16,720 --> 00:38:20,520
llm as an evaluator where um to evaluate

967
00:38:20,520 --> 00:38:23,599
this for instance um we provide in the

968
00:38:23,599 --> 00:38:26,119
first part we see how we can give it a

969
00:38:26,119 --> 00:38:28,440
point-wise evaluation prompt very we

970
00:38:28,440 --> 00:38:32,200
carefully craft The Prompt for an llm to

971
00:38:32,200 --> 00:38:35,480
to evaluate the response of another lm's

972
00:38:35,480 --> 00:38:38,119
response with respect to what the prompt

973
00:38:38,119 --> 00:38:40,920
that was provided and it evaluates it in

974
00:38:40,920 --> 00:38:42,960
a with a score of one to5 with respect

975
00:38:42,960 --> 00:38:45,240
to a carefully crafted rubrics which we

976
00:38:45,240 --> 00:38:48,599
have defined here and uh we see how this

977
00:38:48,599 --> 00:38:51,240
can be used and it gives some reasoning

978
00:38:51,240 --> 00:38:53,880
as well as a score and we see here that

979
00:38:53,880 --> 00:38:56,200
uh we get a score as well as the

980
00:38:56,200 --> 00:38:59,319
reasoning behind it as well as well then

981
00:38:59,319 --> 00:39:02,839
we play around to see uh like how you

982
00:39:02,839 --> 00:39:05,400
can improve or reduce the score and what

983
00:39:05,400 --> 00:39:07,599
makes a good prompt so explaining for

984
00:39:07,599 --> 00:39:09,760
example explaining our technical reports

985
00:39:09,760 --> 00:39:12,680
to a 5-year-old is obviously going to

986
00:39:12,680 --> 00:39:16,119
lead to a slightly lower uh response by

987
00:39:16,119 --> 00:39:17,680
the evaluator because we often have the

988
00:39:17,680 --> 00:39:19,440
word puppy which is not present in our

989
00:39:19,440 --> 00:39:22,280
technical report so good way toig to see

990
00:39:22,280 --> 00:39:24,000
the difference and we get a very

991
00:39:24,000 --> 00:39:26,760
expected score of one and in the last

992
00:39:26,760 --> 00:39:28,640
part of our col lab um we discuss

993
00:39:28,640 --> 00:39:31,520
various techniques for using evaluation

994
00:39:31,520 --> 00:39:34,040
in practice for instance we discuss

995
00:39:34,040 --> 00:39:36,920
pointwise evaluation um where for

996
00:39:36,920 --> 00:39:39,319
summarization where we kind of take a

997
00:39:39,319 --> 00:39:41,319
response take a prompt which generated a

998
00:39:41,319 --> 00:39:44,400
response and have an llm evaluation

999
00:39:44,400 --> 00:39:47,240
evaluator determine on a score on a

1000
00:39:47,240 --> 00:39:49,839
scale of one to five what score does it

1001
00:39:49,839 --> 00:39:52,480
get however it could be because the the

1002
00:39:52,480 --> 00:39:54,760
scale of 1 to five is not very fine

1003
00:39:54,760 --> 00:39:57,000
grained that uh there's a tie between

1004
00:39:57,000 --> 00:39:59,319
some responses and this is where

1005
00:39:59,319 --> 00:40:02,119
point-wise evaluation is uh sometimes

1006
00:40:02,119 --> 00:40:04,319
does not suffice and it's often useful

1007
00:40:04,319 --> 00:40:05,960
to have

1008
00:40:05,960 --> 00:40:09,640
um um um pairwise evaluation uh as well

1009
00:40:09,640 --> 00:40:11,760
where we uh where we give two responses

1010
00:40:11,760 --> 00:40:14,359
to a particular prompt and have the llm

1011
00:40:14,359 --> 00:40:16,960
as a judge select that response this is

1012
00:40:16,960 --> 00:40:20,920
what we also see and then uh uh and then

1013
00:40:20,920 --> 00:40:24,359
uh we finally end the co uh the collab

1014
00:40:24,359 --> 00:40:28,040
with um seeing how we can uh it's often

1015
00:40:28,040 --> 00:40:30,400
um useful as enen mentioned earlier to

1016
00:40:30,400 --> 00:40:33,440
generate multiple responses by the llm

1017
00:40:33,440 --> 00:40:35,520
athor judge instead of just selecting

1018
00:40:35,520 --> 00:40:37,960
the first response to ensure that the

1019
00:40:37,960 --> 00:40:40,720
score that you get is not just due to

1020
00:40:40,720 --> 00:40:42,280
noise and uh

1021
00:40:42,280 --> 00:40:45,359
stochasticity so yeah so it's a lot to

1022
00:40:45,359 --> 00:40:49,520
cover but um off to you page for the pop

1023
00:40:49,520 --> 00:40:52,240
quiz excellent thank you so much Anand

1024
00:40:52,240 --> 00:40:55,440
and to Mark McDonald uh who uh helped

1025
00:40:55,440 --> 00:40:57,920
create many of these code labs

1026
00:40:57,920 --> 00:40:59,640
um youall have done a great job of

1027
00:40:59,640 --> 00:41:01,599
making all of the concepts that are

1028
00:41:01,599 --> 00:41:03,119
being discussed in the white papers and

1029
00:41:03,119 --> 00:41:06,200
in the Q&A sections real uh and I'm

1030
00:41:06,200 --> 00:41:07,920
really looking forward to seeing what

1031
00:41:07,920 --> 00:41:10,000
people build and uh and their initial

1032
00:41:10,000 --> 00:41:12,319
impressions of the code Labs so this is

1033
00:41:12,319 --> 00:41:15,520
very very cool thank you um with that

1034
00:41:15,520 --> 00:41:18,839
I'm going to go ahead and move into the

1035
00:41:18,839 --> 00:41:21,640
uh the pop quiz um so I'm going to bring

1036
00:41:21,640 --> 00:41:23,800
up onto the screen some questions that

1037
00:41:23,800 --> 00:41:25,599
hopefully folks will be able to answer

1038
00:41:25,599 --> 00:41:27,599
now that you've had this uh now that

1039
00:41:27,599 --> 00:41:29,800
you've had this 24-hour crash course in

1040
00:41:29,800 --> 00:41:31,280
prompt engineering and foundational

1041
00:41:31,280 --> 00:41:33,920
models um to start with our first

1042
00:41:33,920 --> 00:41:36,359
question which Gemini configuration

1043
00:41:36,359 --> 00:41:38,079
setting controls the degree of

1044
00:41:38,079 --> 00:41:40,359
Randomness in the selection of the next

1045
00:41:40,359 --> 00:41:44,200
predicted token is it temperature is it

1046
00:41:44,200 --> 00:41:48,040
top K is it top P or is it the output

1047
00:41:48,040 --> 00:41:51,640
token count um remember back to uh to

1048
00:41:51,640 --> 00:41:53,000
the white paper as well as some of the

1049
00:41:53,000 --> 00:41:55,000
questions that Kieran was answering

1050
00:41:55,000 --> 00:41:58,040
today which Gemini configuration setting

1051
00:41:58,040 --> 00:42:00,280
controls the degree of Randomness and

1052
00:42:00,280 --> 00:42:03,640
the selection of the next predicted

1053
00:42:03,640 --> 00:42:06,000
token so hopefully everybody's had a

1054
00:42:06,000 --> 00:42:08,599
chance to jot this down on either a a

1055
00:42:08,599 --> 00:42:10,839
pen uh or a piece of paper with a pen or

1056
00:42:10,839 --> 00:42:13,319
a pencil um or if you're just kind of

1057
00:42:13,319 --> 00:42:16,200
taking notes in a dock um but the answer

1058
00:42:16,200 --> 00:42:19,000
is a temperature um so hopefully

1059
00:42:19,000 --> 00:42:22,000
hopefully everyone got this right um

1060
00:42:22,000 --> 00:42:24,720
question two which of the following is

1061
00:42:24,720 --> 00:42:27,680
not a technique used to accelerate

1062
00:42:27,680 --> 00:42:31,160
in large language models um is it

1063
00:42:31,160 --> 00:42:34,280
quantization is it distillation is it

1064
00:42:34,280 --> 00:42:37,359
flash attention or is it fine-tuning um

1065
00:42:37,359 --> 00:42:40,000
again and you're looking for uh what is

1066
00:42:40,000 --> 00:42:42,400
not a technique to accelerate inference

1067
00:42:42,400 --> 00:42:44,960
in large language

1068
00:42:44,960 --> 00:42:52,400
models and I countdown five 4 3 2 one

1069
00:42:52,400 --> 00:42:55,079
and the correct answer is D fine-tuning

1070
00:42:55,079 --> 00:42:57,480
fine tuning is not a technique used to

1071
00:42:57,480 --> 00:42:59,160
accelerate

1072
00:42:59,160 --> 00:43:01,599
inference question number three which of

1073
00:43:01,599 --> 00:43:04,000
the following is a unique characteristic

1074
00:43:04,000 --> 00:43:06,359
of the Gemini family of large language

1075
00:43:06,359 --> 00:43:09,480
models is it a Gemini models were the

1076
00:43:09,480 --> 00:43:11,079
first to introduce the concept of

1077
00:43:11,079 --> 00:43:14,000
unsupervised pre-training B Gemini

1078
00:43:14,000 --> 00:43:17,359
models can support multimodal inputs C

1079
00:43:17,359 --> 00:43:20,400
Gemini models are decoder only or D

1080
00:43:20,400 --> 00:43:22,599
Gemini models can support a context

1081
00:43:22,599 --> 00:43:24,760
window of up to 2 million tokens what is

1082
00:43:24,760 --> 00:43:27,119
a unique characteristic of the Gemini

1083
00:43:27,119 --> 00:43:29,960
family of large language models and I

1084
00:43:29,960 --> 00:43:32,520
countdown five

1085
00:43:32,520 --> 00:43:39,800
4 3 2 one the correct answer is D Gemini

1086
00:43:39,800 --> 00:43:41,680
models can support a context window of

1087
00:43:41,680 --> 00:43:43,839
up to 2 million tokens and hopefully if

1088
00:43:43,839 --> 00:43:45,200
you've been experimenting with some of

1089
00:43:45,200 --> 00:43:48,079
our Pro Models in AI dodev um which is

1090
00:43:48,079 --> 00:43:50,359
Google AI Studio you should have been

1091
00:43:50,359 --> 00:43:52,880
experimenting this uh with this

1092
00:43:52,880 --> 00:43:55,359
firsthand question number four how does

1093
00:43:55,359 --> 00:43:57,119
reinforcement learning from Human

1094
00:43:57,119 --> 00:44:00,240
feedback rhf improve large language

1095
00:44:00,240 --> 00:44:02,960
models is it a by training the model on

1096
00:44:02,960 --> 00:44:06,599
a massive data set of unlabeled text is

1097
00:44:06,599 --> 00:44:08,800
it B by using a reward model to

1098
00:44:08,800 --> 00:44:10,480
incentivize the generation of human

1099
00:44:10,480 --> 00:44:13,839
preferred responses is it C by reducing

1100
00:44:13,839 --> 00:44:15,520
the number of parameters in the model

1101
00:44:15,520 --> 00:44:18,760
for faster inference um or is a d by

1102
00:44:18,760 --> 00:44:20,400
converting the model into a recurrent

1103
00:44:20,400 --> 00:44:22,400
neural network for improved performance

1104
00:44:22,400 --> 00:44:25,200
how does rhf improve large language

1105
00:44:25,200 --> 00:44:27,920
models

1106
00:44:27,920 --> 00:44:29,680
and hopefully everybody remembers this a

1107
00:44:29,680 --> 00:44:31,160
little bit from the from the white

1108
00:44:31,160 --> 00:44:33,240
papers as well as through some of the

1109
00:44:33,240 --> 00:44:35,440
questions that we were answering today

1110
00:44:35,440 --> 00:44:42,520
I'm going to count down five 4 3 2 1 and

1111
00:44:42,520 --> 00:44:45,480
the correct answer is B um rhf uses a

1112
00:44:45,480 --> 00:44:47,359
reward bottle to incentivize the

1113
00:44:47,359 --> 00:44:49,680
generation of human preferred

1114
00:44:49,680 --> 00:44:52,240
responses question number five which

1115
00:44:52,240 --> 00:44:54,480
technique enhances an lm's reasoning

1116
00:44:54,480 --> 00:44:56,640
abilities by Pro by prompting it to

1117
00:44:56,640 --> 00:44:58,400
produce intermediate reasoning steps

1118
00:44:58,400 --> 00:45:02,000
leading to more accurate answers is it a

1119
00:45:02,000 --> 00:45:05,240
zero shot prompting B step back

1120
00:45:05,240 --> 00:45:08,520
prompting C self-consistent prompting or

1121
00:45:08,520 --> 00:45:11,760
D Chain of Thought

1122
00:45:12,040 --> 00:45:14,160
prompting hopefully everyone is thinking

1123
00:45:14,160 --> 00:45:17,040
back to the white papers um and

1124
00:45:17,040 --> 00:45:18,800
hopefully you've also been experimenting

1125
00:45:18,800 --> 00:45:20,359
with this prompting technique as you

1126
00:45:20,359 --> 00:45:22,880
were uh as you were kind of playing with

1127
00:45:22,880 --> 00:45:25,040
the Gemini models in AI Studio as well

1128
00:45:25,040 --> 00:45:28,960
as in your kagle code labs

1129
00:45:29,160 --> 00:45:30,640
but the answer

1130
00:45:30,640 --> 00:45:33,720
is D Chain of Thought prompting Chain of

1131
00:45:33,720 --> 00:45:35,680
Thought prompting helps the model show

1132
00:45:35,680 --> 00:45:37,960
intermediate reasoning steps which often

1133
00:45:37,960 --> 00:45:41,559
leads to more accurate answers um so

1134
00:45:41,559 --> 00:45:43,359
thank you to everyone for for

1135
00:45:43,359 --> 00:45:45,359
participating today hopefully you all

1136
00:45:45,359 --> 00:45:48,800
scored 100% correct on your pop quiz uh

1137
00:45:48,800 --> 00:45:50,480
and if you didn't you learned something

1138
00:45:50,480 --> 00:45:52,960
along the way so thank you for uh thank

1139
00:45:52,960 --> 00:45:56,000
you for kind of testing your your new

1140
00:45:56,000 --> 00:45:58,040
Knowledge and Skills and

1141
00:45:58,040 --> 00:46:00,800
capabilities um and the the last

1142
00:46:00,800 --> 00:46:03,480
question what is a minimum GPU memory

1143
00:46:03,480 --> 00:46:05,559
needed for inference on a three billion

1144
00:46:05,559 --> 00:46:08,280
parameter model using standard float

1145
00:46:08,280 --> 00:46:11,400
Precision um this is kind of a an extra

1146
00:46:11,400 --> 00:46:13,280
bonus question which you should have

1147
00:46:13,280 --> 00:46:14,839
been reading the white papers in order

1148
00:46:14,839 --> 00:46:19,800
to answer um is it three G uh three

1149
00:46:19,800 --> 00:46:22,800
gigabyte six 12 or

1150
00:46:22,800 --> 00:46:26,720
24 um how much GPU memory would you need

1151
00:46:26,720 --> 00:46:30,319
to to run a 3 billion parameter

1152
00:46:30,319 --> 00:46:34,960
model and the correct answer is 12 um so

1153
00:46:34,960 --> 00:46:36,920
hopefully hopefully everyone got this

1154
00:46:36,920 --> 00:46:40,040
right um and if not um refer back to the

1155
00:46:40,040 --> 00:46:43,480
white paper to to learn more so thank

1156
00:46:43,480 --> 00:46:46,839
you so much uh again for dialing In from

1157
00:46:46,839 --> 00:46:48,960
from all of the the folks that are

1158
00:46:48,960 --> 00:46:50,160
working on our

1159
00:46:50,160 --> 00:46:53,559
q&as um the kaggle team the Google deep

1160
00:46:53,559 --> 00:46:56,280
mine team the organizing team a huge

1161
00:46:56,280 --> 00:46:58,880
round of applause for everybody involved

1162
00:46:58,880 --> 00:47:01,280
um thank you so much and look forward to

1163
00:47:01,280 --> 00:47:04,680
seeing you tomorrow
