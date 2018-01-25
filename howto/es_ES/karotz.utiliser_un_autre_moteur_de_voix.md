conecte telnet
======================

Primero debe conectarse telnet (puerto 23) en openkarotz,
el identificador de ser kartoz

Adición de un motor de la voz
=========================

Ir a / www / cgi-bin / y editar el archivo tts.inc, añadir una
función (por ejemplo Jeedom):

    {jeedomTTS función
       TTS = $ 1
       MD5File = $ (echo "$ TTS" | md5sum | cut -d '' -f 1)
       eval $ (echo "rizar -A '$ {AU}' -o $ CNF_DATADIR / tmp / $ {} .mp3 MD5File http: //TODO/core/api/tts.php TODO apikey = & texto = $ {} TTS " ') >> / dev / null 2 ​​>> / dev / null
       echo $ (echo "$ RAW_TTS" | urldecode)> $ CNF_DATADIR / tmp / $ {} .txt MD5File
       if [ "$ 5" = "1"!] entonces
            Log "[TTS]" "sonido Jugando} $ {MD5File .mp3"
            PlaySound $ CNF_DATADIR / tmp / $ {} .mp3 MD5File
        fi
        if [ "$ NOCACHE" == "1"]; entonces
            rm -f $ CNF_DATADIR / tmp / $ {} .mp3 MD5File >> / dev / null 2 ​​>> / dev / null
            rm -f $ CNF_DATADIR / tmp / $ {} .txt MD5File >> / dev / null 2 ​​>> / dev / null
         otro
            Log "[TTS]" "Almacenamiento de sonido $ {} .mp3 MD5File para almacenar en caché"
         fi
       echo $ {} MD5File
    }

A continuación, edite el archivo y añadir TTS:

    3) MP3_Id = $ ($ jeedomTTS TTS VOICE $ $ $ no_cache RAW_VOICE) ;;

En la "caja \ $ TTS \ _ENGINE en" tener:

     $ TTS_ENGINE en caja
                 1) MP3_Id = $ ($ GoogleTTS TTS VOICE $ $ $ no_cache RAW_VOICE) ;;
                 2) MP3_Id = $ ($ VioletTTS TTS VOICE $ $ $ no_cache RAW_VOICE) ;;
                 3) MP3_Id = $ ($ jeedomTTS TTS VOICE $ $ $ no_cache RAW_VOICE) ;;
                 *) = $ MP3_Id (AcapelaTTS $ voz TTS $ $ $ $ no_cache RAW_VOICE MUTE) ;;
    esac

uso
===========

Sólo appller URL que indica el número de vehículos (en este caso 3):

    http://192.168.0.62/cgi-bin/tts?text=coucou%20ca%20va&nocache=0&engine=3
