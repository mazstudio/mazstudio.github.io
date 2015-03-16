---
layout: post
category: jekyll
title: Mac OSX 에서 Jekyll Theme 설치 시 오류 해결 방법
date: 2015-03-16 16:55
tags: jekyll
comments: true
---


Jekyll테마를 적용할 때 `bundle install` 을 해서 설치하는 경우가 있습니다. 이 명령어를 실행할 때, Mac상에서 아래와 같은 오류가 나면서 실패하는 경우가 있습니다.  
  

	`Make sure that 'gem install nokogiri -v '버전명'' succeeds before bundling.`

이 경우, nokogiri설치가 실패되어서 그런 것 인데, 아래 명령어로 설치할 수 있습니다. (Yosemite 기준)

	`gem install nokogiri -- --with-xml2-include=/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX10.10.sdk/usr/include/libxml2 --use-system-libraries`


하위 맥 버전이나, 추가사항은 아래 출처를 참고해주세요. :)

***
출처 : [stackoverflow]("http://stackoverflow.com/questions/19643153/error-to-install-nokogiri-on-osx-10-9-maverick")
