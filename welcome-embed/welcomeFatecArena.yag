{{ $user := .User }}
{{ $bot := "" }}
{{ if $user.Bot }} {{ $bot = print "_<a:setar:870331984386347038> Este usuário é um _**__BOT__**, _mas mesmo assim desejamos sempre boas-vindas!_ <a:heyy:813476527458746378>"}} {{ end }}

{{$title := print  "" .User.Username " acaba de entrar na arena!"}}

{{$avatar := .User.AvatarURL "256"}}
{{$desc := (joinStr "" .User.Mention ", seja bem-vindo à Fatec Arena! 🎮👊 E para começar,  [leia as regras](https://discord.com/channels/1087093963418247318/1087094482589188156) para garantir que todos se divirtam em um ambiente justo e saudável. " $bot)}}

{{$embed := cembed
    "title" $title
    "color" 5292589
    "description" $desc
    "timestamp" currentTime
    "author" (sdict "name" .User.String "icon_url" (.User.AvatarURL "512"))
    "thumbnail" (sdict "url" $avatar) 
    "image" (sdict
        "url" "https://i.ibb.co/zfV94vD/farena.png")
    
    "footer" (sdict
        "text" "Fatec Arena • ©️ Todos os direitos reservados.")
}}

{{sendMessage nil $embed}}