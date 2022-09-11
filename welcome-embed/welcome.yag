{{ $user := .User }}
{{ $bot := "" }}
{{ if $user.Bot }} {{ $bot = print "_<a:setar:870331984386347038> Este usuário se trata de um _**__BOT__**, _mas de qualquer forma desejamos sempre boas vindas_ <a:heyy:813476527458746378>"}}  {{ end }}

{{$title := print "<a:ztw:809897478031802429>  | " .User.Username " acabou de entrar no ɢʜɪʙʟɪ ʜᴏᴜsᴇ"}}

{{$avatar := .User.AvatarURL "256" }}
{{$desc := (joinStr "" .User.Mention " Divirta-se e por favor, [Registre-se](https://discord.com/channels/833192426898063430/835771580651012116) e  [Leia as regras](https://discord.com/channels/833192426898063430/833206414662041610) antes de qualquer coisa! <:happy:873716334461075496> \n " $bot)}}
{{$embed := cembed
    "title" $title
    "color" 5292589
    "description" $desc
    "timestamp" currentTime
    "author" (sdict "name" .User.String "icon_url" (.User.AvatarURL "512"))
    "thumbnail" (sdict "url" $avatar) 
    "image" (sdict
        "url" "https://i.ibb.co/sP91yVz/bannerb.png")
    
    "footer" (sdict
        "text" "🌸ɢʜɪʙʟɪ ʜᴏᴜsᴇ𝚎🌸 • ©️ Todos os direitos reservados.")
}}
{{sendMessage nil $embed}}