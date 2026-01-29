<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>MySocial (Full)</title>
    <style>
        :root {
            --bg-color: #ffffff;
            --text-color: #000000;
            --sidebar-bg: #f4f4f5;
            --primary-color: #3390ec;
            --secondary-bg: #ffffff;
            --border-color: #dfe1e5;
            --message-out: #eeffde;
            --message-in: #f2f2f2;
            --input-bg: #f4f4f5;
            --nav-height: 60px;
            --danger-color: #ff4444;
        }

        [data-theme="dark"] {
            --bg-color: #0f0f0f;
            --text-color: #ffffff;
            --sidebar-bg: #1c1c1d;
            --primary-color: #8774e1;
            --secondary-bg: #212121;
            --border-color: #2b2b2b;
            --message-out: #8774e1;
            --message-in: #212121;
            --input-bg: #1c1c1d;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            margin: 0; padding: 0;
            background-color: var(--bg-color);
            color: var(--text-color);
            height: 100vh; height: 100dvh;
            display: flex; overflow: hidden;
        }

        /* --- UI Elements --- */
        .hidden { display: none !important; }
        .action-btn { 
            padding: 8px 16px; border-radius: 8px; border: none; 
            background: var(--primary-color); color: white; font-weight: bold; cursor: pointer;
        }
        input, textarea {
            width: 100%; padding: 12px; margin: 5px 0;
            border: 1px solid var(--border-color); border-radius: 10px;
            background: var(--input-bg); color: var(--text-color);
            box-sizing: border-box; font-family: inherit; font-size: 16px;
        }

        /* --- Layout --- */
        #auth-screen {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: var(--bg-color); display: flex; justify-content: center; align-items: center; z-index: 2000;
        }
        .auth-box {
            background: var(--secondary-bg); padding: 30px; border-radius: 16px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1); width: 90%; max-width: 350px; text-align: center;
            border: 1px solid var(--border-color);
        }

        #app-screen { display: none; width: 100%; height: 100%; }
        
        .sidebar {
            width: 250px; background: var(--sidebar-bg);
            border-right: 1px solid var(--border-color);
            display: flex; flex-direction: column; padding: 10px; flex-shrink: 0;
        }
        .main-content {
            flex: 1; display: flex; flex-direction: column;
            background: var(--bg-color); overflow: hidden; position: relative;
        }
        .view {
            display: none; padding: 15px; overflow-y: auto; height: 100%;
            padding-bottom: 80px; box-sizing: border-box;
        }
        .view.active { display: block; }

        /* Navigation */
        .nav-item {
            padding: 12px; border-radius: 10px; cursor: pointer; margin-bottom: 5px;
            display: flex; align-items: center; color: var(--text-color);
        }
        .nav-item.active { background-color: rgba(128,128,128, 0.15); font-weight: bold; }
        .nav-icon { margin-right: 10px; font-size: 1.2em; }

        /* --- Components --- */
        .post-card, .user-item {
            background: var(--secondary-bg); border: 1px solid var(--border-color);
            border-radius: 12px; padding: 15px; margin-bottom: 12px; position: relative;
        }
        
        /* Avatar Styles */
        .avatar-small {
            width: 40px; height: 40px; border-radius: 50%; object-fit: cover;
            background: #ccc; margin-right: 10px; flex-shrink: 0;
        }
        .avatar-large {
            width: 80px; height: 80px; border-radius: 50%; object-fit: cover;
            background: #ccc; margin-bottom: 10px;
        }
        .user-row { display: flex; align-items: center; }

        .post-header {
            display: flex; align-items: center; margin-bottom: 8px; cursor: pointer;
        }
        .post-author-name { font-weight: bold; color: var(--primary-color); }
        .post-date { font-size: 0.75em; color: gray; margin-left: auto; }
        .post-image {
            width: 100%; height: auto; border-radius: 8px; margin-top: 10px;
            border: 1px solid var(--border-color);
        }
        .delete-btn {
            color: var(--danger-color); cursor: pointer; font-size: 1.2em; padding: 5px;
        }

        /* Profile Specifics */
        .profile-header { text-align: center; margin-bottom: 15px; }
        .stats-row { 
            display: flex; justify-content: center; gap: 20px; margin: 15px 0; 
        }
        .stat-item { cursor: pointer; text-align: center; }
        .stat-num { font-weight: bold; font-size: 1.2em; display: block; }
        .stat-label { font-size: 0.9em; color: gray; }

        /* Modals */
        .modal-overlay {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.5); z-index: 3000;
            display: none; justify-content: center; align-items: center;
        }
        .modal-content {
            background: var(--secondary-bg); width: 90%; max-width: 400px;
            padding: 20px; border-radius: 12px; max-height: 80vh; overflow-y: auto;
        }
        .modal-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 15px; }
        .close-modal { font-size: 1.5em; cursor: pointer; }

        /* Chat */
        .messages-area { flex: 1; overflow-y: auto; padding: 15px; display: flex; flex-direction: column; gap: 8px; }
        .message-bubble {
            max-width: 75%; padding: 10px 14px; border-radius: 18px;
            position: relative; word-wrap: break-word; font-size: 15px;
            display: flex; flex-direction: column;
        }
        .msg-own { align-self: flex-end; background: var(--message-out); color: var(--text-color); border-bottom-right-radius: 4px; }
        .msg-other { align-self: flex-start; background: var(--message-in); border: 1px solid var(--border-color); border-bottom-left-radius: 4px; }
        .msg-delete { font-size: 10px; color: #ff4444; align-self: flex-end; margin-top: 5px; cursor: pointer; opacity: 0.7;}

        /* Mobile */
        @media (max-width: 768px) {
            #app-screen { flex-direction: column; }
            .sidebar {
                position: fixed; bottom: 0; left: 0; width: 100%; height: var(--nav-height);
                flex-direction: row; justify-content: space-around;
                border-top: 1px solid var(--border-color); padding: 0; z-index: 100;
                background: var(--sidebar-bg); backdrop-filter: blur(10px); -webkit-backdrop-filter: blur(10px);
            }
            .sidebar h3, .desktop-only { display: none; }
            .nav-item { flex-direction: column; font-size: 10px; flex: 1; justify-content: center; padding: 5px; margin: 0;}
            .nav-icon { margin: 0 0 2px 0; font-size: 20px; }
            .nav-logout { display: none !important; }
            #view-chat-room {
                position: fixed; top: 0; left: 0; width: 100%; height: 100dvh;
                background: var(--bg-color); z-index: 200; padding: 0; display: none; flex-direction: column;
            }
        }
    </style>
</head>
<body>

    <div id="auth-screen">
        <div class="auth-box" id="login-box">
            <h2>Вход</h2>
            <input type="text" id="login-username" placeholder="Юзернейм">
            <input type="password" id="login-password" placeholder="Пароль">
            <button class="action-btn" style="width:100%; margin-top:10px;" onclick="app.login()">Войти</button>
            <p style="color:var(--primary-color); cursor:pointer; margin-top:15px;" onclick="ui.toggleAuth('register')">Создать аккаунт</p>
        </div>
        <div class="auth-box hidden" id="register-box">
            <h2>Регистрация</h2>
            <input type="text" id="reg-username" placeholder="Никнейм">
            <input type="password" id="reg-password" placeholder="Пароль">
            <button class="action-btn" style="width:100%; margin-top:10px;" onclick="app.register()">Готово</button>
            <p style="color:var(--primary-color); cursor:pointer; margin-top:15px;" onclick="ui.toggleAuth('login')">Назад</p>
        </div>
    </div>

    <div id="edit-profile-modal" class="modal-overlay">
        <div class="modal-content">
            <div class="modal-header"><h3>Редактировать профиль</h3><span class="close-modal" onclick="ui.closeModals()">×</span></div>
            <div style="text-align:center;">
                <img id="edit-avatar-preview" class="avatar-large">
                <br>
                <label class="action-btn" style="font-size:0.9em;">
                    Загрузить фото
                    <input type="file" hidden accept="image/*" onchange="app.handleAvatarSelect(this)">
                </label>
            </div>
            <textarea id="edit-bio" placeholder="О себе..." rows="3" style="margin-top:15px;"></textarea>
            <button class="action-btn" style="width:100%; margin-top:10px;" onclick="app.saveProfile()">Сохранить</button>
        </div>
    </div>

    <div id="user-list-modal" class="modal-overlay">
        <div class="modal-content">
            <div class="modal-header"><h3 id="user-list-title">Список</h3><span class="close-modal" onclick="ui.closeModals()">×</span></div>
            <div id="user-list-content"></div>
        </div>
    </div>

    <div id="app-screen">
        <div class="sidebar">
            <h3 class="desktop-only" style="padding-left:12px; margin-bottom: 20px;">MySocial</h3>
            <div class="nav-item active" onclick="ui.navigate('feed')"><span class="nav-icon">📰</span><span>Лента</span></div>
            <div class="nav-item" onclick="ui.navigate('chats')"><span class="nav-icon">💬</span><span>Чаты</span></div>
            <div class="nav-item" onclick="ui.navigate('profile', app.user.username)"><span class="nav-icon">👤</span><span>Профиль</span></div>
            <div class="nav-item" onclick="ui.navigate('settings')"><span class="nav-icon">⚙️</span><span>Меню</span></div>
            <div class="nav-item nav-logout" style="margin-top: auto; color: red;" onclick="app.logout()"><span class="nav-icon">🚪</span><span>Выйти</span></div>
        </div>

        <div class="main-content">
            <div id="view-feed" class="view active">
                <div class="post-card">
                    <textarea id="new-post-text" placeholder="Что у вас нового?"></textarea>
                    <div style="display:flex; justify-content:space-between; align-items:center; margin-top:5px;">
                        <label style="cursor:pointer; font-size:1.5em;">📷<input type="file" hidden accept="image/*" onchange="app.handlePhotoSelect(this)"></label>
                        <button class="action-btn" onclick="app.createPost()">Опубликовать</button>
                    </div>
                    <img id="image-preview" class="post-image hidden">
                </div>
                <div id="feed-container"></div>
            </div>

            <div id="view-profile" class="view">
                <div id="profile-content"></div>
                <h3>Посты</h3>
                <div id="profile-posts"></div>
            </div>

            <div id="view-chats" class="view">
                <h2>Чаты</h2>
                <div id="friends-list"></div>
            </div>

            <div id="view-chat-room" class="view" style="padding:0; display:none; flex-direction:column;">
                <div style="padding:10px 15px; border-bottom:1px solid var(--border-color); background:var(--sidebar-bg); display:flex; align-items:center;">
                    <button onclick="ui.navigate('chats')" style="background:none; border:none; font-size:1.5em; margin-right:10px; color:var(--text-color);">←</button>
                    <b id="chat-with-name">User</b>
                </div>
                <div class="messages-area" id="messages-container"></div>
                <div style="padding:10px; background:var(--sidebar-bg); display:flex; gap:10px; border-top:1px solid var(--border-color); padding-bottom: env(safe-area-inset-bottom, 10px);">
                    <input type="text" id="message-input" placeholder="Сообщение..." autocomplete="off" style="margin:0; border-radius:20px; padding-left:15px;">
                    <button class="action-btn" style="border-radius:50%; width:45px; height:45px; padding:0; display:flex; justify-content:center; align-items:center;" onclick="app.sendMessage()">➤</button>
                </div>
            </div>

            <div id="view-settings" class="view">
                <h2>Настройки</h2>
                <div class="post-card">
                    <label style="display:flex; align-items:center; gap:10px; font-size:1.1em;">
                        <input type="checkbox" id="theme-toggle" onchange="ui.toggleTheme()" style="width:20px; height:20px;"> 
                        Тёмная тема
                    </label>
                </div>
                <button class="action-btn" style="background-color: var(--danger-color); margin-top: 20px;" onclick="app.logout()">Выйти из аккаунта</button>
            </div>
        </div>
    </div>

<script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/9.22.0/firebase-app.js";
    import { getFirestore, collection, addDoc, getDocs, doc, setDoc, getDoc, updateDoc, deleteDoc, arrayUnion, arrayRemove, onSnapshot, query, orderBy, where } from "https://www.gstatic.com/firebasejs/9.22.0/firebase-firestore.js";

    // 🔴 КЛЮЧИ
    const firebaseConfig = {
      apiKey: "AIzaSyBCcBSZx6kAFGwTscJlfDuiQILGZDaVN4g",
      authDomain: "mysocnet-34ee9.firebaseapp.com",
      projectId: "mysocnet-34ee9",
      storageBucket: "mysocnet-34ee9.firebasestorage.app",
      messagingSenderId: "82449086862",
      appId: "1:82449086862:web:e77a61b33a54be97a00cdf",
      measurementId: "G-4Z2SMZS5N4"
    };

    const firebaseApp = initializeApp(firebaseConfig);
    const db = getFirestore(firebaseApp);

    let activeChatUnsub = null;
    let feedUnsub = null;
    let tempImage = null; // Для поста
    let tempAvatar = null; // Для профиля

    // Утилита для сжатия фото
    const compressImage = (file, callback) => {
        const reader = new FileReader();
        reader.readAsDataURL(file);
        reader.onload = (e) => {
            const img = new Image();
            img.src = e.target.result;
            img.onload = () => {
                const canvas = document.createElement('canvas');
                const MAX = 600;
                let w = img.width, h = img.height;
                if (w > h) { if (w > MAX) { h *= MAX/w; w = MAX; } } 
                else { if (h > MAX) { w *= MAX/h; h = MAX; } }
                canvas.width = w; canvas.height = h;
                const ctx = canvas.getContext('2d');
                ctx.drawImage(img, 0, 0, w, h);
                callback(canvas.toDataURL('image/jpeg', 0.7));
            };
        };
    };

    window.app = {
        user: null,

        init: async () => {
            if(localStorage.getItem('theme') === 'dark') {
                document.documentElement.setAttribute('data-theme', 'dark');
                document.getElementById('theme-toggle').checked = true;
            }
            const savedUser = localStorage.getItem('my_social_user');
            if (savedUser) {
                try {
                    const docSnap = await getDoc(doc(db, "users", savedUser));
                    if (docSnap.exists()) {
                        app.user = docSnap.data();
                        ui.showApp();
                    } else ui.showAuth();
                } catch (e) { ui.showAuth(); }
            } else ui.showAuth();
        },

        register: async () => {
            const username = document.getElementById('reg-username').value.trim().toLowerCase();
            const password = document.getElementById('reg-password').value.trim();
            if (!username || !password) return alert('Заполните поля');
            try {
                const userRef = doc(db, "users", username);
                const userSnap = await getDoc(userRef);
                if (userSnap.exists()) return alert('Никнейм занят');
                await setDoc(userRef, { username, password, followers: [], following: [], bio: '', avatar: '' });
                alert('Готово! Войдите.'); ui.toggleAuth('login');
            } catch (e) { alert("Ошибка Firebase"); }
        },

        login: async () => {
            const username = document.getElementById('login-username').value.trim().toLowerCase();
            const password = document.getElementById('login-password').value.trim();
            try {
                const userSnap = await getDoc(doc(db, "users", username));
                if (userSnap.exists() && userSnap.data().password === password) {
                    app.user = userSnap.data();
                    localStorage.setItem('my_social_user', username);
                    ui.showApp();
                } else alert('Неверно');
            } catch (e) { alert("Ошибка"); }
        },
        logout: () => { localStorage.removeItem('my_social_user'); location.reload(); },

        // --- Profile Editing ---
        handleAvatarSelect: (input) => {
            if(input.files[0]) compressImage(input.files[0], (base64) => {
                tempAvatar = base64;
                document.getElementById('edit-avatar-preview').src = base64;
            });
        },
        saveProfile: async () => {
            const bio = document.getElementById('edit-bio').value.trim();
            const updates = { bio: bio };
            if (tempAvatar) updates.avatar = tempAvatar;
            
            await updateDoc(doc(db, "users", app.user.username), updates);
            // Update local cache
            app.user.bio = bio; 
            if(tempAvatar) app.user.avatar = tempAvatar;
            
            ui.closeModals();
            ui.renderProfile(app.user.username);
        },

        // --- Posts ---
        handlePhotoSelect: (input) => {
            if(input.files[0]) compressImage(input.files[0], (base64) => {
                tempImage = base64;
                const prev = document.getElementById('image-preview');
                prev.src = base64; prev.classList.remove('hidden');
            });
        },
        createPost: async () => {
            const text = document.getElementById('new-post-text').value.trim();
            if (!text && !tempImage) return;
            const post = { author: app.user.username, content: text, createdAt: Date.now() };
            if (tempImage) { post.image = tempImage; post.authorAvatar = app.user.avatar || ''; } // Cache avatar in post for speed
            else { post.authorAvatar = app.user.avatar || ''; }
            
            await addDoc(collection(db, "posts"), post);
            document.getElementById('new-post-text').value = '';
            document.getElementById('image-preview').classList.add('hidden');
            tempImage = null;
        },
        deletePost: async (id) => {
            if(confirm("Удалить пост?")) await deleteDoc(doc(db, "posts", id));
        },

        // --- Interactions ---
        follow: async (target) => {
            const myRef = doc(db, "users", app.user.username);
            const targetRef = doc(db, "users", target);
            if (app.user.following.includes(target)) {
                await updateDoc(myRef, { following: arrayRemove(target) });
                await updateDoc(targetRef, { followers: arrayRemove(app.user.username) });
                app.user.following = app.user.following.filter(u => u !== target);
            } else {
                await updateDoc(myRef, { following: arrayUnion(target) });
                await updateDoc(targetRef, { followers: arrayUnion(app.user.username) });
                app.user.following.push(target);
            }
            ui.renderProfile(target);
        },
        sendMessage: async () => {
            const text = document.getElementById('message-input').value.trim();
            if (!text || !window.currentChatPartner) return;
            const chatId = [app.user.username, window.currentChatPartner].sort().join('_');
            await addDoc(collection(db, "chats", chatId, "messages"), {
                sender: app.user.username, text, timestamp: Date.now()
            });
            document.getElementById('message-input').value = '';
        },
        deleteMessage: async (msgId) => {
            const chatId = [app.user.username, window.currentChatPartner].sort().join('_');
            if(confirm("Удалить сообщение?")) 
                await deleteDoc(doc(db, "chats", chatId, "messages", msgId));
        }
    };

    window.ui = {
        toggleAuth: (mode) => {
            document.getElementById('login-box').classList.toggle('hidden', mode !== 'login');
            document.getElementById('register-box').classList.toggle('hidden', mode !== 'register');
        },
        showAuth: () => {
            document.getElementById('auth-screen').style.display = 'flex';
            document.getElementById('app-screen').style.display = 'none';
        },
        showApp: () => {
            document.getElementById('auth-screen').style.display = 'none';
            document.getElementById('app-screen').style.display = 'flex';
            ui.navigate('feed');
        },
        navigate: (view, param) => {
            if (activeChatUnsub) activeChatUnsub();
            if (view !== 'feed' && feedUnsub) feedUnsub();
            document.querySelectorAll('.view').forEach(el => el.classList.remove('active'));
            if(view !== 'chat-room') document.getElementById('view-chat-room').style.display = 'none';
            document.querySelectorAll('.nav-item').forEach(el => el.classList.remove('active'));
            
            // Highlight nav
            const map = {'feed':0, 'chats':1, 'profile':2, 'settings':3};
            if(map[view]!==undefined) document.querySelectorAll('.nav-item')[map[view]].classList.add('active');

            if (view === 'feed') { document.getElementById('view-feed').classList.add('active'); ui.renderFeed(); }
            else if (view === 'profile') { document.getElementById('view-profile').classList.add('active'); ui.renderProfile(param || app.user.username); }
            else if (view === 'chats') { document.getElementById('view-chats').classList.add('active'); ui.renderChatsList(); }
            else if (view === 'chat-room') {
                window.currentChatPartner = param;
                document.getElementById('view-chat-room').style.display = 'flex';
                ui.renderChatRoom(param);
            } else if (view === 'settings') { document.getElementById('view-settings').classList.add('active'); }
        },
        
        closeModals: () => document.querySelectorAll('.modal-overlay').forEach(el => el.style.display = 'none'),

        // --- Renderers ---
        renderFeed: () => {
            const container = document.getElementById('feed-container');
            feedUnsub = onSnapshot(query(collection(db, "posts"), orderBy("createdAt", "desc")), async (snapshot) => {
                container.innerHTML = '';
                for (const docSnap of snapshot.docs) {
                    const post = docSnap.data();
                    const id = docSnap.id;
                    
                    // Fetch avatar if needed (simple cache logic usually needed here, but kept simple)
                    let avatarSrc = post.authorAvatar || '';
                    if (!avatarSrc) {
                        // Fallback: try to fetch user avatar
                        // (Skipping for performance in simple feed, usually stored in post)
                    }

                    const isMine = post.author === app.user.username;
                    const delBtn = isMine ? `<span class="delete-btn" onclick="app.deletePost('${id}')">🗑️</span>` : '';
                    const imgHtml = post.image ? `<img src="${post.image}" class="post-image">` : '';
                    const avatarHtml = `<img src="${avatarSrc || 'https://via.placeholder.com/40'}" class="avatar-small">`;

                    const div = document.createElement('div');
                    div.className = 'post-card';
                    div.innerHTML = `
                        <div class="post-header" onclick="ui.navigate('profile', '${post.author}')">
                            ${avatarHtml}
                            <span class="post-author-name">@${post.author}</span>
                            <span class="post-date">${new Date(post.createdAt).toLocaleDateString()}</span>
                        </div>
                        <div>${post.content}</div>
                        ${imgHtml}
                        ${delBtn ? `<div style="text-align:right; margin-top:5px;">${delBtn}</div>` : ''}
                    `;
                    container.appendChild(div);
                }
            });
        },

        renderProfile: async (username) => {
            const container = document.getElementById('profile-content');
            const postsContainer = document.getElementById('profile-posts');
            container.innerHTML = 'Загрузка...';
            
            const userSnap = await getDoc(doc(db, "users", username));
            if (!userSnap.exists()) return container.innerHTML = 'Нет такого пользователя';
            
            const user = userSnap.data();
            const isMe = username === app.user.username;
            const isFollowing = app.user.following.includes(username);
            const isFriend = user.followers.includes(app.user.username) && user.following.includes(app.user.username);

            let mainBtn = '';
            if (isMe) {
                mainBtn = `<button class="action-btn" onclick="ui.openEditProfile()">Редактировать</button>`;
            } else {
                mainBtn = `<button class="action-btn" style="background:${isFollowing?'gray':'var(--primary-color)'}" onclick="app.follow('${username}')">${isFollowing?'Отписаться':'Подписаться'}</button>`;
                if(isFriend) mainBtn += `<button class="action-btn" style="margin-left:10px; background:#4caf50;" onclick="ui.navigate('chat-room', '${username}')">Чат</button>`;
            }

            container.innerHTML = `
                <div class="post-card profile-header">
                    <div style="display:flex; justify-content:center;">
                        <img src="${user.avatar || 'https://via.placeholder.com/80'}" class="avatar-large">
                    </div>
                    <h2>@${user.username}</h2>
                    <p style="color:gray;">${user.bio || 'Нет информации'}</p>
                    
                    <div class="stats-row">
                        <div class="stat-item" onclick="ui.openUserList('followers', '${username}')">
                            <span class="stat-num">${user.followers.length}</span>
                            <span class="stat-label">Подписчики</span>
                        </div>
                        <div class="stat-item" onclick="ui.openUserList('following', '${username}')">
                            <span class="stat-num">${user.following.length}</span>
                            <span class="stat-label">Подписки</span>
                        </div>
                    </div>
                    ${mainBtn}
                </div>
            `;

            // User posts
            const postSnaps = await getDocs(query(collection(db, "posts"), where("author", "==", username), orderBy("createdAt", "desc")));
            postsContainer.innerHTML = '';
            postSnaps.forEach(docSnap => {
                const post = docSnap.data();
                const id = docSnap.id;
                const isMine = post.author === app.user.username; // Should be true here always if isMe
                const delBtn = isMe ? `<span class="delete-btn" onclick="app.deletePost('${id}'); this.parentElement.parentElement.remove();">🗑️</span>` : '';
                const imgHtml = post.image ? `<img src="${post.image}" class="post-image">` : '';
                
                const div = document.createElement('div');
                div.className = 'post-card';
                div.innerHTML = `<div class="post-header"><span class="post-author-name">@${post.author}</span><span class="post-date">${new Date(post.createdAt).toLocaleDateString()}</span></div><div>${post.content}</div>${imgHtml}${delBtn ? `<div style="text-align:right;">${delBtn}</div>`:''}`;
                postsContainer.appendChild(div);
            });
        },

        openEditProfile: () => {
            document.getElementById('edit-bio').value = app.user.bio || '';
            document.getElementById('edit-avatar-preview').src = app.user.avatar || 'https://via.placeholder.com/80';
            document.getElementById('edit-profile-modal').style.display = 'flex';
        },

        openUserList: async (type, username) => {
            const modal = document.getElementById('user-list-modal');
            const title = document.getElementById('user-list-title');
            const content = document.getElementById('user-list-content');
            
            title.innerText = type === 'followers' ? 'Подписчики' : 'Подписки';
            content.innerHTML = 'Загрузка...';
            modal.style.display = 'flex';

            const userSnap = await getDoc(doc(db, "users", username));
            const list = userSnap.data()[type]; // array of usernames

            content.innerHTML = '';
            if(list.length === 0) content.innerHTML = '<p>Пусто</p>';

            for(const uName of list) {
                // Fetch basic info just to show avatar? Or just list name
                // Keeping it fast: just name and action
                const div = document.createElement('div');
                div.className = 'user-item';
                div.style.display = 'flex'; div.style.justifyContent = 'space-between'; div.style.alignItems = 'center';
                
                let btn = '';
                // If I am viewing my own "following" list, show Unfollow button
                if (username === app.user.username && type === 'following') {
                    btn = `<button class="action-btn" style="font-size:0.8em; padding:5px 10px; background:gray;" onclick="app.follow('${uName}'); this.parentElement.remove();">Отписаться</button>`;
                }

                div.innerHTML = `<b onclick="ui.navigate('profile', '${uName}'); ui.closeModals();">@${uName}</b> ${btn}`;
                content.appendChild(div);
            }
        },

        renderChatsList: async () => {
            const container = document.getElementById('friends-list');
            container.innerHTML = 'Обновление...';
            // Refresh self
            app.user = (await getDoc(doc(db, "users", app.user.username))).data();
            let html = '';
            
            for (const fName of app.user.following) {
                const fSnap = await getDoc(doc(db, "users", fName));
                if (fSnap.exists() && fSnap.data().following.includes(app.user.username)) {
                    const fData = fSnap.data();
                    html += `<div class="user-item user-row" onclick="ui.navigate('chat-room', '${fName}')">
                        <img src="${fData.avatar || 'https://via.placeholder.com/40'}" class="avatar-small">
                        <div>
                            <div style="font-weight:bold">@${fName}</div>
                            <div style="color:var(--primary-color); font-size:0.9em">Написать</div>
                        </div>
                    </div>`;
                }
            }
            container.innerHTML = html || '<div style="text-align:center; padding:20px; color:gray">Нужна взаимная подписка</div>';
        },

        renderChatRoom: (partner) => {
            document.getElementById('chat-with-name').innerText = '@' + partner;
            const container = document.getElementById('messages-container');
            const chatId = [app.user.username, partner].sort().join('_');
            
            activeChatUnsub = onSnapshot(query(collection(db, "chats", chatId, "messages"), orderBy("timestamp", "asc")), (snapshot) => {
                container.innerHTML = '';
                snapshot.forEach(docSnap => {
                    const msg = docSnap.data();
                    const id = docSnap.id;
                    const isOwn = msg.sender === app.user.username;
                    const div = document.createElement('div');
                    div.className = `message-bubble ${isOwn ? 'msg-own' : 'msg-other'}`;
                    div.innerHTML = `<span>${msg.text}</span> ${isOwn ? `<span class="msg-delete" onclick="app.deleteMessage('${id}')">удалить</span>` : ''}`;
                    container.appendChild(div);
                });
                container.scrollTop = container.scrollHeight;
            });
        },
        toggleTheme: () => {
            const isDark = document.getElementById('theme-toggle').checked;
            document.documentElement.setAttribute('data-theme', isDark ? 'dark' : '');
            localStorage.setItem('theme', isDark ? 'dark' : 'light');
        }
    };
    app.init();
</script>
</body>
</html>
