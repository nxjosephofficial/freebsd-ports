PORTNAME=	argc
DISTVERSIONPREFIX=	v
DISTVERSION=	1.16.0
CATEGORIES=	devel

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Easily parse command line arguments in bash
WWW=		https://github.com/sigoden/argc

LICENSE=	APACHE20 MIT
LICENSE_COMB=	dual
LICENSE_FILE_APACHE20=	${WRKSRC}/LICENSE-APACHE
LICENSE_FILE_MIT=	${WRKSRC}/LICENSE-MIT

USES=		cargo

USE_GITHUB=	yes
GH_ACCOUNT=	sigoden

CARGO_CRATES=	aho-corasick-1.1.3 \
		anstyle-1.0.6 \
		anyhow-1.0.81 \
		assert_cmd-2.0.14 \
		assert_fs-1.1.1 \
		autocfg-1.2.0 \
		base64-0.22.0 \
		bitflags-1.3.2 \
		bitflags-2.5.0 \
		bstr-1.9.1 \
		cfg-if-1.0.0 \
		console-0.15.8 \
		convert_case-0.6.0 \
		crossbeam-deque-0.8.5 \
		crossbeam-epoch-0.9.18 \
		crossbeam-utils-0.8.19 \
		difflib-0.4.0 \
		dirs-5.0.1 \
		dirs-sys-0.4.1 \
		doc-comment-0.3.3 \
		either-1.10.0 \
		encode_unicode-0.3.6 \
		equivalent-1.0.1 \
		errno-0.3.8 \
		fastrand-2.0.2 \
		float-cmp-0.9.0 \
		futures-0.3.30 \
		futures-channel-0.3.30 \
		futures-core-0.3.30 \
		futures-executor-0.3.30 \
		futures-io-0.3.30 \
		futures-macro-0.3.30 \
		futures-sink-0.3.30 \
		futures-task-0.3.30 \
		futures-timer-3.0.3 \
		futures-util-0.3.30 \
		getrandom-0.2.12 \
		glob-0.3.1 \
		globset-0.4.14 \
		globwalk-0.9.1 \
		hashbrown-0.14.3 \
		hermit-abi-0.3.9 \
		home-0.5.9 \
		ignore-0.4.22 \
		indexmap-2.2.6 \
		insta-1.36.1 \
		itoa-1.0.10 \
		lazy_static-1.4.0 \
		libc-0.2.153 \
		libredox-0.0.1 \
		linked-hash-map-0.5.6 \
		linux-raw-sys-0.4.13 \
		log-0.4.21 \
		memchr-2.7.1 \
		minimal-lexical-0.2.1 \
		natord-1.0.9 \
		nom-7.1.3 \
		normalize-line-endings-0.3.0 \
		num-traits-0.2.18 \
		num_cpus-1.16.0 \
		option-ext-0.2.0 \
		pin-project-lite-0.2.13 \
		pin-utils-0.1.0 \
		predicates-3.1.0 \
		predicates-core-1.0.6 \
		predicates-tree-1.0.9 \
		proc-macro2-1.0.79 \
		quote-1.0.35 \
		redox_syscall-0.4.1 \
		redox_users-0.4.4 \
		regex-1.10.4 \
		regex-automata-0.4.6 \
		regex-syntax-0.8.2 \
		relative-path-1.9.2 \
		roff-0.2.1 \
		rstest-0.18.2 \
		rstest_macros-0.18.2 \
		rustc_version-0.4.0 \
		rustix-0.38.32 \
		ryu-1.0.17 \
		same-file-1.0.6 \
		semver-1.0.22 \
		serde-1.0.197 \
		serde_derive-1.0.197 \
		serde_json-1.0.114 \
		shell-words-1.1.0 \
		similar-2.4.0 \
		slab-0.4.9 \
		smawk-0.3.2 \
		syn-2.0.55 \
		tempfile-3.10.1 \
		termtree-0.4.1 \
		textwrap-0.16.1 \
		thiserror-1.0.58 \
		thiserror-impl-1.0.58 \
		threadpool-1.8.1 \
		unicode-ident-1.0.12 \
		unicode-linebreak-0.1.5 \
		unicode-segmentation-1.11.0 \
		unicode-width-0.1.11 \
		wait-timeout-0.2.0 \
		walkdir-2.5.0 \
		wasi-0.11.0+wasi-snapshot-preview1 \
		which-6.0.1 \
		winapi-0.3.9 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.6 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		windows-sys-0.48.0 \
		windows-sys-0.52.0 \
		windows-targets-0.48.5 \
		windows-targets-0.52.4 \
		windows_aarch64_gnullvm-0.48.5 \
		windows_aarch64_gnullvm-0.52.4 \
		windows_aarch64_msvc-0.48.5 \
		windows_aarch64_msvc-0.52.4 \
		windows_i686_gnu-0.48.5 \
		windows_i686_gnu-0.52.4 \
		windows_i686_msvc-0.48.5 \
		windows_i686_msvc-0.52.4 \
		windows_x86_64_gnu-0.48.5 \
		windows_x86_64_gnu-0.52.4 \
		windows_x86_64_gnullvm-0.48.5 \
		windows_x86_64_gnullvm-0.52.4 \
		windows_x86_64_msvc-0.48.5 \
		windows_x86_64_msvc-0.52.4 \
		winsafe-0.0.19 \
		yaml-rust-0.4.5

PLIST_FILES=	bin/${PORTNAME}

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
