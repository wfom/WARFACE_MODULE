# Патч-ноут WF DEV SDK

## Информация про оригинальную сборку (ту, которая дошла до автора репозитория)

Наже преставлены источники файлов, которые были использованы для того, чтобы вернуть работоспособность редактору.

Warface 1.22400.5519.45100:
- \[Bin64\Cry3DEngine.dll\]
- \[Bin64\CryAction.dll\]
- \[Bin64\CryAISystem.dll\]
- \[Bin64\CryAnimation.dll\]
- \[Bin64\CryEntitySystem.dll\]
- \[Bin64\CryFont.dll\]
- \[Bin64\CryGame.dll\]
- \[Bin64\CryInput.dll\]
- \[Bin64\CryMovie.dll\]
- \[Bin64\CryNetwork.dll\]
- \[Bin64\CryOnline.dll\]
- \[Bin64\CryPhysics.dll\]
- \[Bin64\CryRenderD3D9.dll\]
- \[Bin64\CryRenderNULL.dll\]
- \[Bin64\CryScriptSystem.dll\]
- \[Bin64\CrySoundSystem.dll\]
- \[Bin64\CrySystem.dll\]
- \[Bin64\DedicatedServer.exe\]
- \[Bin64\Editor.exe\]
- \[Bin64\Game.exe\]
- \[Bin64\EnableAIDevMode.reg\]

Warface RU 1.22100.2077.41200 от 17.08.2020
- \[Engine/*\]
- \[Game/*\]

Warface RU 1.22600.2114.17100 от 08.09.2020
- \[Bin64\api-ms-win-core-file-l1-2-0.dll\]
- \[Bin64\api-ms-win-core-file-l2-1-0.dll\]
- \[Bin64\api-ms-win-core-localization-l1-2-0.dll\]
- \[Bin64\api-ms-win-core-processthreads-l1-1-1.dll\]
- \[Bin64\api-ms-win-core-synch-l1-2-0.dll\]
- \[Bin64\api-ms-win-core-timezone-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-convert-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-environment-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-filesystem-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-heap-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-locale-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-math-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-multibyte-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-runtime-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-stdio-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-string-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-time-l1-1-0.dll\]
- \[Bin64\api-ms-win-crt-utility-l1-1-0.dll\]
- \[Bin64\D3DX9_42.dll\]
- \[Bin64\msvcp140.dll\]
- \[Bin64\ucrtbase.dll\]
- \[Bin64\vcruntime140.dll\]
- \[Bin64\steam_appid.txt\]
- \[Bin64\CrashRpt1402.dll\]
- \[Bin64\OptickCore.dll\]
- \[Bin64\cohtml.WindowsDesktop.dll\]
- \[Bin64\v8.dll\]
- \[Bin64\RenoirCore.WindowsDesktop.dll\]
- \[Bin64\v8_libbase.dll\]
- \[Bin64\sonus.dll\]
- \[Bin64\vivoxsdk_x64.dll\]
- \[Bin64\discord_game_sdk.dll\]
- \[Bin64\GfeSDK.dll\]
- \[Bin64\GFSDK_GSA.win64.dll\]
- \[Bin64\steam_api64.dll\]
- \[Bin64\ortp_x64.dll\]
- \[Bin64\pcnsl.exe\]

Warface RU PTS 1.20600.1897.41200:
- \[Bin64\ocevogyv.dll\]

Неизвестный источник:
- \[Bin64\fmod_event_netL64.dll\]
- \[Bin64\fmod_eventL64.dll\]
- \[Bin64\fmodexL64.dll\]

Hallowed Encounter 5.3.4.47:
- \[Bin64\ToolkitPro1340vc140x64.dll\]

CryEngine 3.4.5.6666:
- \[Bin64\libTIFF64.dll\]
- \[Bin64\SHAllocator.dll\]
- \[Bin64\LuaCompiler.exe\]

dlltop.ru:
- \[Bin64\mfc140.dll\]
- \[Bin64\vcruntime140_1.dll\]

Собственная компиляция:
- \[Bin64\TestBot.dll\]

## Изменения в редакторе WF DEV SDK версии сборки 1.0.1, в сравнении с той версией, в какой она дошла до автора

- Добавлен Resource Compiler \[Bin32\rc\\] от CryEngine 3.3.8, благодаря этому появилась возможность:
	- создавать собственные CubeMaps (текстуры для EnvironmentProbe);
 	- конвертировать собственные текстуры в формат, который подходит редактору;
- Изменён стандартный TOD (Time Of Day) в файле \[Editor\default_time_of_day.tod\] для более приятной графики на первых этапах создания уровня;
- Изменена стандартная текстура Terrain (на такую же как в CryEngine 3.3.8, так как варфейсовская полностью белая и не имеет разметки);
- Обновлены значения параметров графики в архиве \[Engine\Engine.pak\], а именно в файлах:
	- \[config\cvargroups\sys_spec_quality.cfg\]
	- \[config\cvargroups\sys_spec_shading.cfg\]
 	- \[config\cvargroups\sys_spec_shadows.cfg\]
  	- \[config\cvargroups\sys_spec_sound.cfg\]
  	- \[config\cvargroups\sys_spec_texture.cfg\]
- Дополнение \[Game\Z_Other.pak\], которое было создано для исправления некоторых ошибок, распаковано в директорию, а также были удалены следующие файлы:
	- \[config\ai_debug.cfg\]
 	- \[config\ai_debug.cfg\]
	- \[config\avarst.cfg\]
	- \[config\cheats.cfg\]
	- \[config\ctf_test.cfg\]
	- \[config\directortest.cfg\]
	- \[config\end_game.cfg\]
	- \[config\latency_crit.cfg\]
	- \[config\latency_high.cfg\]
	- \[config\latency_low.cfg\]
	- \[config\latency_mid.cfg\]
	- \[config\latency_zero.cfg\]
	- \[config\mission_generator.cfg\]
	- \[config\no_rod.cfg\]
	- \[config\pregame.cfg\]
	- \[config\ptb_test.cfg\]
	- \[config\resource_leak.cfg\]
	- \[config\resourcecheck.cfg\]
	- \[config\ssao_off.cfg\]
	- \[config\ssao_on.cfg\]
	- \[config\stress_srv.cfg\]
	- \[config\test_level.cfg\]
	- \[config\uif.cfg\]
- Полностью обновлены файлы \[Game\config\system.cfg\] и \[Game\config\editor.cfg\], а именно обновлены значения кваров на актуальные, исправлено множество графических моментов, а ненужные квары были удалены;
- В постоянную директорию вынесен файл \[Game\Libs\config\DefaultProfile.xml\], так как в него были внесены правки для добавления возможности менять модули оружия на клавиши "8", "9", "0" клавиатуры, так как через HUD это сделать нельзя, из-за курсора CryEngine, который игра не видит;
- В постоянную директорию вынесен файл \[Game\Libs\config\presets\EditorSoldier.lua\], так как в него были внесены правки для возможности менять персонажу следующие параметры: оружие, броню, внешность, модули и боеприпасы (по умолчанию в него были прописаны все модули и боеприпасы клиента 08.2020, но закоментированы, чтобы ускорить загрузку, при необходимости вам лиш нужно будет расскоментировать нужный файл);
- Папка "Профиля" теперь будет записываться в корневую папку редактора, чтобы не конфликтовать с оригинальной папкой "Профиля" Warface;
