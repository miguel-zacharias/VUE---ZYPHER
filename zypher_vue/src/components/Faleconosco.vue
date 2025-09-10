
<template>
	<div class="contact-page">
		<header class="contact-header">
			<div class="logo-title">
				<span class="logo-icon"> <svg width="32" height="32" viewBox="0 0 24 24" fill="none"><path d="M2 12C2 6.477 6.477 2 12 2s10 4.477 10 10-4.477 10-10 10S2 17.523 2 12Zm2 0c0 4.418 3.582 8 8 8a7.963 7.963 0 0 0 6.32-3.16l-2.12-1.6A5.978 5.978 0 0 1 12 18c-3.314 0-6-2.686-6-6H4Zm8-8C7.582 4 4 7.582 4 12h2c0-3.314 2.686-6 6-6 1.657 0 3.156.672 4.24 1.76l1.6-2.12A7.963 7.963 0 0 0 12 4Z" fill="#fff"/></svg> </span>
				<span class="logo-text">Zypher Sneakers</span>
			</div>
			<div class="search-bar">
				<input type="text" placeholder="Pesquisar..." />
				<span class="search-icon">🔍</span>
			</div>
			<div class="header-icons">
				<span class="crown">👑</span>
				<span class="user">👤</span>
				<span class="cart">🛒</span>
			</div>
		</header>
		<nav class="contact-nav">
			<a>FEMININO</a>
			<a>MASCULINO</a>
			<a>INFANTIL</a>
			<a>ESPORTE</a>
		</nav>

		.contact-nav {
			background: #e3e7ee;
			display: flex;
			justify-content: center;
			gap: 40px;
			font-size: 1rem;
			font-family: 'Arial', sans-serif;
			font-weight: 500;
			padding: 8px 0 4px 0;
			color: #000;
		}
		.contact-nav a {
			text-decoration: none;
			color: #000;
			padding: 0 8px;
		}
		.header-icons {
			display: flex;
			align-items: center;
			gap: 18px;
			font-size: 1.3rem;
			color: #000;
		}
		.logo-title {
			display: flex;
			align-items: center;
			font-family: 'Georgia', serif;
			font-size: 1.5rem;
			font-weight: bold;
		}
		.logo-text {
			letter-spacing: 1px;
			color: #000;
		}
		.contact-card {
			background: #fff;
			border-radius: 16px;
			box-shadow: 0 4px 24px rgba(22,41,74,0.07);
			padding: 36px 32px 18px 32px;
			max-width: 420px;
			width: 100%;
			text-align: center;
			color: #000;
		}
		.contact-support {
			background: #f8f8f9;
			border-radius: 8px;
			padding: 14px 12px 10px 12px;
			margin-top: 10px;
			font-size: 1rem;
			color: #000;
			text-align: left;
		}
		.chat-link {
			color: #000;
			text-decoration: underline;
		}
	margin-right: 10px;
	display: flex;
	align-items: center;
}
.logo-text {
	letter-spacing: 1px;
}
.search-bar {
	display: flex;
	align-items: center;
	background: #fff;
	border-radius: 20px;
	padding: 2px 12px;
	min-width: 220px;
}
.search-bar input {
	border: none;
	outline: none;
	font-size: 1rem;
	background: transparent;
	padding: 6px 0;
	width: 150px;
}
.search-icon {
	font-size: 1.2rem;
	margin-left: 4px;
	color: #333;
}
.header-icons {
	display: flex;
	align-items: center;
	gap: 18px;
	font-size: 1.3rem;
}
.contact-nav {
	background: #e3e7ee;
	display: flex;
	justify-content: center;
	gap: 40px;
	font-size: 1rem;
	font-family: 'Arial', sans-serif;
	font-weight: 500;
	padding: 8px 0 4px 0;
	color: #16294a;
}
.contact-nav a {
	text-decoration: none;
	color: #16294a;
	padding: 0 8px;
}
.contact-main {
	flex: 1;
	display: flex;
	justify-content: center;
	align-items: center;
	padding: 40px 0 0 0;
}
.contact-card {
	background: #fff;
	border-radius: 16px;
	box-shadow: 0 4px 24px rgba(22,41,74,0.07);
	padding: 36px 32px 18px 32px;
	max-width: 420px;
	width: 100%;
	text-align: center;
}
.contact-card h1 {
	color: #16294a;
	font-size: 2rem;
	margin-bottom: 8px;
	font-family: 'Arial Black', Arial, sans-serif;
}
.subtitle {
	color: #222;
	font-size: 1.05rem;
	margin-bottom: 18px;
}
.contact-form {
	display: flex;
	flex-direction: column;
	gap: 10px;
	margin-bottom: 18px;
}
.form-label {
	text-align: left;
	font-weight: 600;
	color: #16294a;
	margin-bottom: 2px;
}
.form-select, .form-input, .form-textarea {
	border: 1px solid #d1d5db;
	border-radius: 6px;
	padding: 8px 10px;
	font-size: 1rem;
	font-family: inherit;
	background: #f8f8f9;
	margin-bottom: 2px;
}
.form-select {
	cursor: pointer;
}
.form-textarea {
	min-height: 70px;
	resize: vertical;
}
.form-btn {
	background: #16294a;
	color: #fff;
	border: none;
	border-radius: 6px;
	padding: 12px 0;
	font-size: 1.1rem;
	font-weight: bold;
	cursor: pointer;
	margin-top: 8px;
	transition: background 0.2s;
}
.form-btn:hover {
	background: #0e1a33;
}
.contact-support {
	background: #f8f8f9;
	border-radius: 8px;
	padding: 14px 12px 10px 12px;
	margin-top: 10px;
	font-size: 1rem;
	color: #222;
	text-align: left;
}
.chat-link {
	color: #007bff;
	text-decoration: underline;
}
.contact-footer {
	text-align: center;
	color: #888;
	font-size: 0.95rem;
	padding: 18px 0 8px 0;
	background: transparent;
}
</style>
