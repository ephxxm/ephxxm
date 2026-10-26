
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Digital Space</title>

    <style>
        /* GENERAL PAGE STYLE */
        * {
            box-sizing: border-box;
        }

        body {
            background-color: #070b08;
            color: #c0e9ca;
            font-family: "Courier New", monospace;
            margin: 0;
            padding: 40px 20px;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* MAIN WINDOW */
        .window {
            width: 100%;
            max-width: 850px;
            border: 1px solid #55ff88;
            box-shadow: 0 0 15px #123d22;
            background-color: #0b120d;
        }

        /* TOP BAR */
        .title-bar {
            padding: 18px 22px;
            border-bottom: 1px dashed #28643b;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 15px;
        }

        .title-bar h1 {
            color: #55ff88;
            font-size: clamp(18px, 4vw, 28px);
            margin: 0;
            text-shadow: 0 0 8px #1c743a;
        }

        .window-buttons {
            color: #55ff88;
            white-space: nowrap;
        }

        /* NAVIGATION TABS */
        .tabs {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            padding: 15px 20px 0;
            border-bottom: 1px solid #28643b;
        }

        .tabs a {
            display: inline-block;
            color: #8bbf99;
            border: 1px solid #28643b;
            padding: 10px 14px;
            text-decoration: none;
            font-size: 13px;
        }

        .tabs a:hover,
        .tabs a.active {
            color: #55ff88;
            background-color: #102819;
            border-color: #55ff88;
        }

        /* ADDRESS BAR */
        .toolbar {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 12px 20px;
            border-bottom: 1px solid #28643b;
        }

        .toolbar-button {
            color: #55ff88;
            border: 1px solid #28643b;
            padding: 7px 10px;
            background: transparent;
            font-family: inherit;
            cursor: pointer;
        }

        .address {
            color: #70d991;
            border: 1px solid #28643b;
            padding: 8px 12px;
            flex: 1;
            min-width: 0;
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: nowrap;
        }

        /* MAIN CONTENT */
        .content {
            padding: 20px;
        }

        .profile {
            display: grid;
            grid-template-columns: minmax(130px, 0.8fr) minmax(0, 1.5fr);
            gap: 22px;
        }

        /* PROFILE IMAGE AREA */
        .profile-card {
            border: 1px solid #28643b;
            padding: 10px;
            text-align: center;
            align-self: start;
        }

        .avatar {
            aspect-ratio: 1 / 1;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            background-color: #102819;
            border: 1px dashed #55ff88;
            color: #55ff88;
            font-size: 13px;
            line-height: 1.8;
        }

        .username {
            color: #55ff88;
            margin: 15px 0 5px;
            overflow-wrap: anywhere;
        }

        /* PROFILE INFORMATION */
        .terminal-label {
            color: #55ff88;
            font-size: 13px;
            margin: 0 0 14px;
        }

        .section-title {
            color: #55ff88;
            font-size: 18px;
            margin: 0 0 12px;
        }

        .info {
            line-height: 1.8;
            overflow-wrap: anywhere;
        }

        .info p {
            margin: 8px 0;
        }

        .label {
            color: #55ff88;
        }

        .divider {
            border: none;
            border-top: 1px dashed #28643b;
            margin: 16px 0;
        }

        /* FOOTER */
        footer {
            border-top: 1px dashed #28643b;
            padding: 14px;
            text-align: center;
            color: #4e9867;
            font-size: 12px;
        }

        /* SMALL SCREENS */
        @media (max-width: 520px) {
            body {
                padding: 15px 10px;
                align-items: flex-start;
            }

            .title-bar {
                padding: 15px;
            }

            .window-buttons {
                font-size: 11px;
            }

            .toolbar {
                padding: 10px;
                gap: 6px;
            }

            .toolbar-button {
                padding: 6px;
            }

            .content {
                padding: 12px;
            }

            .profile {
                grid-template-columns: 1fr;
            }

            .profile-card {
                width: 100%;
                max-width: 220px;
                justify-self: center;
            }
        }
    </style>
</head>

<body>

    <main class="window">

        <!-- WINDOW HEADER -->
        <header class="title-bar">
            <h1> YOU FOUND ME! </h1>
            <div class="window-buttons">[ _ ] [ □ ] [ X ]</div>
        </header>

        <!-- NAVIGATION -->
        <nav class="tabs">
            <a href="#home" class="active">[ HOME ]</a>
            <a href="#about">[ ABOUT ]</a>
            <a href="#interests">[ INTERESTS ]</a>
            <a href="#links">[ LINKS ]</a>
        </nav>

        <!-- BROWSER TOOLBAR -->
        <div class="toolbar">
            <button class="toolbar-button"
                    onclick="history.back()"
                    aria-label="Go back">&lt;</button>

            <button class="toolbar-button"
                    onclick="history.forward()"
                    aria-label="Go forward">&gt;</button>

            <span class="address">https://myspace.local/</span>

            <button class="toolbar-button"
                    onclick="location.reload()"
                    aria-label="Reload page">&#8635;</button>
        </div>

        <!-- WEBSITE CONTENT -->
        <div class="content" id="home">

            <p class="terminal-label">
                user@myspace:~$ whoami
            </p>

            <div class="profile">

                <!-- LEFT SIDE -->
                <aside class="profile-card">

                    <div class="avatar">
                        <pre>
 ╱|、
(` - 7
|、⁻〵
  じしˍ,)ノ
                        </pre> 
                        <span>[ MEOW ]</span>
                    </div>

                    <p class="username">@masvvyo</p>

                    <p class="terminal-label">
                        [ add me on discord? ]
                    </p>

                </aside>

                <!-- RIGHT SIDE -->
                <section class="info" id="about">

                    <h2 class="section-title">
                        MAYO's BIDDINGS
                    </h2>

                    <p>
                        <span class="label">name:</span>
                        Mayo
                    </p>

                    <p>
                        <span class="label">status:</span>
                        ● on hiatus
                    </p>

                    <p>
                        <span class="label">about me:</span>
                        I'm just playing around with my digital space, trying to make it look like a terminal. I like cats, music, and coding.
                    </p>

                    <hr class="divider">

                    <div id="interests">
                        <p class="terminal-label">
                            Interests:
                        </p>

                        <p>
                            art / music / games 
                        </p>
                    </div>

                    <hr class="divider">

                    <div id="links"> <nav class="tabs">
                        <p class="terminal-label">
                            links:
                        </p>

                        <p align="center">
                            <a href="https://github.com/ephxxm"
                               style="color: #55ff88;">
                                [ GITHUB ]
                            </a>
                        </p>
                        
                        <p align="center">
                            <a href="https://ephemeral.atabook.org/?page=1"
                               style="color: #55ff88;">
                                [ ATA ]
                            </a>
                        </p>
                    </div> </nav>

                </section>

            </div>
        </div>

        <!-- FOOTER -->
        <footer>
            @2024 Mayo's Digital Space.
        </footer>

    </main>

</body>
</html>
