# HtmlDemo
## 哈哈哈





<!doctype html>
<html lang="zh" class="no-js">
  <head>
    
      <meta charset="utf-8">
      <meta name="viewport" content="width=device-width,initial-scale=1">
      <meta http-equiv="x-ua-compatible" content="ie=edge">
      
        <meta name="description" content="Stories About C Plus Plus">
      
      
      
        <meta name="author" content="光城">
      
      
        <meta name="lang:clipboard.copy" content="复制">
      
        <meta name="lang:clipboard.copied" content="已复制">
      
        <meta name="lang:search.language" content="ja">
      
        <meta name="lang:search.pipeline.stopwords" content="True">
      
        <meta name="lang:search.pipeline.trimmer" content="True">
      
        <meta name="lang:search.result.none" content="没有找到符合条件的结果">
      
        <meta name="lang:search.result.one" content="找到 1 个符合条件的结果">
      
        <meta name="lang:search.result.other" content="# 个符合条件的结果">
      
        <meta name="lang:search.tokenizer" content="[\uff0c\u3002]+">
      
      <link rel="shortcut icon" href="../../assets/images/favicon.png">
      <meta name="generator" content="mkdocs-1.1, mkdocs-material-4.6.3">
    
    
      
        <title>const那些事 - C++那些事</title>
      
    
    
      <link rel="stylesheet" href="../../assets/stylesheets/application.adb8469c.css">
      
        <link rel="stylesheet" href="../../assets/stylesheets/application-palette.a8b3c06d.css">
      
      
        
        
        <meta name="theme-color" content="#ef5350">
      
    
    
      <script src="../../assets/javascripts/modernizr.86422ebf.js"></script>
    
    
      
        <link href="https://fonts.gstatic.com" rel="preconnect" crossorigin>
        <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Ubuntu:300,400,400i,700%7CUbuntu+Mono&display=fallback">
        <style>body,input{font-family:"Ubuntu","Helvetica Neue",Helvetica,Arial,sans-serif}code,kbd,pre{font-family:"Ubuntu Mono","Courier New",Courier,monospace}</style>
      
    
    <link rel="stylesheet" href="../../assets/fonts/material-icons.css">
    
    
    
      
    
    
  </head>
  
    
    
    <body dir="ltr" data-md-color-primary="red" data-md-color-accent="red">
  
    <svg class="md-svg">
      <defs>
        
        
          <svg xmlns="http://www.w3.org/2000/svg" width="416" height="448" viewBox="0 0 416 448" id="__github"><path fill="currentColor" d="M160 304q0 10-3.125 20.5t-10.75 19T128 352t-18.125-8.5-10.75-19T96 304t3.125-20.5 10.75-19T128 256t18.125 8.5 10.75 19T160 304zm160 0q0 10-3.125 20.5t-10.75 19T288 352t-18.125-8.5-10.75-19T256 304t3.125-20.5 10.75-19T288 256t18.125 8.5 10.75 19T320 304zm40 0q0-30-17.25-51T296 232q-10.25 0-48.75 5.25Q229.5 240 208 240t-39.25-2.75Q130.75 232 120 232q-29.5 0-46.75 21T56 304q0 22 8 38.375t20.25 25.75 30.5 15 35 7.375 37.25 1.75h42q20.5 0 37.25-1.75t35-7.375 30.5-15 20.25-25.75T360 304zm56-44q0 51.75-15.25 82.75-9.5 19.25-26.375 33.25t-35.25 21.5-42.5 11.875-42.875 5.5T212 416q-19.5 0-35.5-.75t-36.875-3.125-38.125-7.5-34.25-12.875T37 371.5t-21.5-28.75Q0 312 0 260q0-59.25 34-99-6.75-20.5-6.75-42.5 0-29 12.75-54.5 27 0 47.5 9.875t47.25 30.875Q171.5 96 212 96q37 0 70 8 26.25-20.5 46.75-30.25T376 64q12.75 25.5 12.75 54.5 0 21.75-6.75 42 34 40 34 99.5z"/></svg>
        
      </defs>
    </svg>
    <input class="md-toggle" data-md-toggle="drawer" type="checkbox" id="__drawer" autocomplete="off">
    <input class="md-toggle" data-md-toggle="search" type="checkbox" id="__search" autocomplete="off">
    <label class="md-overlay" data-md-component="overlay" for="__drawer"></label>
    
      <a href="#const" tabindex="0" class="md-skip">
        跳转至
      </a>
    
    
      <header class="md-header" data-md-component="header">
  <nav class="md-header-nav md-grid">
    <div class="md-flex">
      <div class="md-flex__cell md-flex__cell--shrink">
        <a href="../.." title="C++那些事" aria-label="C++那些事" class="md-header-nav__button md-logo">
          
            <i class="md-icon"></i>
          
        </a>
      </div>
      <div class="md-flex__cell md-flex__cell--shrink">
        <label class="md-icon md-icon--menu md-header-nav__button" for="__drawer"></label>
      </div>
      <div class="md-flex__cell md-flex__cell--stretch">
        <div class="md-flex__ellipsis md-header-nav__title" data-md-component="title">
          
            <span class="md-header-nav__topic">
              C++那些事
            </span>
            <span class="md-header-nav__topic">
              
                const那些事
              
            </span>
          
        </div>
      </div>
      <div class="md-flex__cell md-flex__cell--shrink">
        
          <label class="md-icon md-icon--search md-header-nav__button" for="__search"></label>
          
<div class="md-search" data-md-component="search" role="dialog">
  <label class="md-search__overlay" for="__search"></label>
  <div class="md-search__inner" role="search">
    <form class="md-search__form" name="search">
      <input type="text" class="md-search__input" aria-label="search" name="query" placeholder="搜索" autocapitalize="off" autocorrect="off" autocomplete="off" spellcheck="false" data-md-component="query" data-md-state="active">
      <label class="md-icon md-search__icon" for="__search"></label>
      <button type="reset" class="md-icon md-search__icon" data-md-component="reset" tabindex="-1">
        &#xE5CD;
      </button>
    </form>
    <div class="md-search__output">
      <div class="md-search__scrollwrap" data-md-scrollfix>
        <div class="md-search-result" data-md-component="result">
          <div class="md-search-result__meta">
            键入以开始搜索
          </div>
          <ol class="md-search-result__list"></ol>
        </div>
      </div>
    </div>
  </div>
</div>
        
      </div>
      
        <div class="md-flex__cell md-flex__cell--shrink">
          <div class="md-header-nav__source">
            


  

<a href="https://github.com/Light-City/CPlusPlusThings" title="前往 Github 仓库" class="md-source" data-md-source="github">
  
    <div class="md-source__icon">
      <svg viewBox="0 0 24 24" width="24" height="24">
        <use xlink:href="#__github" width="24" height="24"></use>
      </svg>
    </div>
  
  <div class="md-source__repository">
    Light-City/CPlusPlusThings
  </div>
</a>
          </div>
        </div>
      
    </div>
  </nav>
</header>
    
    <div class="md-container">
      
        
      
      
      <main class="md-main" role="main">
        <div class="md-main__inner md-grid" data-md-component="container">
          
            
              <div class="md-sidebar md-sidebar--primary" data-md-component="navigation">
                <div class="md-sidebar__scrollwrap">
                  <div class="md-sidebar__inner">
                    <nav class="md-nav md-nav--primary" data-md-level="0">
  <label class="md-nav__title md-nav__title--site" for="__drawer">
    <a href="../.." title="C++那些事" class="md-nav__button md-logo">
      
        <i class="md-icon"></i>
      
    </a>
    C++那些事
  </label>
  
    <div class="md-nav__source">
      


  

<a href="https://github.com/Light-City/CPlusPlusThings" title="前往 Github 仓库" class="md-source" data-md-source="github">
  
    <div class="md-source__icon">
      <svg viewBox="0 0 24 24" width="24" height="24">
        <use xlink:href="#__github" width="24" height="24"></use>
      </svg>
    </div>
  
  <div class="md-source__repository">
    Light-City/CPlusPlusThings
  </div>
</a>
    </div>
  
  <ul class="md-nav__list" data-md-scrollfix>
    
      
      
      


  <li class="md-nav__item">
    <a href="../.." title="项目概要" class="md-nav__link">
      项目概要
    </a>
  </li>

    
      
      
      


  <li class="md-nav__item">
    <a href="../../use/" title="使用须知" class="md-nav__link">
      使用须知
    </a>
  </li>

    
      
      
      

  


  <li class="md-nav__item md-nav__item--active md-nav__item--nested">
    
      <input class="md-toggle md-nav__toggle" data-md-toggle="nav-3" type="checkbox" id="nav-3" checked>
    
    <label class="md-nav__link" for="nav-3">
      基础进阶
    </label>
    <nav class="md-nav" data-md-component="collapsible" data-md-level="1">
      <label class="md-nav__title" for="nav-3">
        基础进阶
      </label>
      <ul class="md-nav__list" data-md-scrollfix>
        
        
          
          
          

  


  <li class="md-nav__item md-nav__item--active">
    
    <input class="md-toggle md-nav__toggle" data-md-toggle="toc" type="checkbox" id="__toc">
    
      
    
    
      <label class="md-nav__link md-nav__link--active" for="__toc">
        const那些事
      </label>
    
    <a href="./" title="const那些事" class="md-nav__link md-nav__link--active">
      const那些事
    </a>
    
      
<nav class="md-nav md-nav--secondary">
  
  
    
  
  
    <label class="md-nav__title" for="__toc">目录</label>
    <ul class="md-nav__list" data-md-scrollfix>
      
        <li class="md-nav__item">
  <a href="#1const" class="md-nav__link">
    1.const含义
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#2const" class="md-nav__link">
    2.const作用
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#3const" class="md-nav__link">
    3.const对象默认为文件局部变量
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#4" class="md-nav__link">
    4.定义常量
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#5const" class="md-nav__link">
    5.指针与const
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#6const" class="md-nav__link">
    6.函数中使用const
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#7const" class="md-nav__link">
    7.类中使用const
  </a>
  
</li>
      
      
      
      
      
    </ul>
  
</nav>
    
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../static/" title="static那些事" class="md-nav__link">
      static那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../this/" title="this那些事" class="md-nav__link">
      this那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../inline/" title="inline那些事" class="md-nav__link">
      inline那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../sizeof/" title="sizeof那些事" class="md-nav__link">
      sizeof那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../abstract/" title="纯虚函数和抽象类那些事" class="md-nav__link">
      纯虚函数和抽象类那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../vptr_vtable/" title="vptr_vtable那些事" class="md-nav__link">
      vptr_vtable那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../virtual/" title="virtual那些事" class="md-nav__link">
      virtual那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../volatile/" title="volatile那些事" class="md-nav__link">
      volatile那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../assert/" title="assert那些事" class="md-nav__link">
      assert那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../bit/" title="位域那些事" class="md-nav__link">
      位域那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../extern/" title="extern那些事" class="md-nav__link">
      extern那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../struct/" title="struct那些事" class="md-nav__link">
      struct那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../struct_class/" title="struct与class那些事" class="md-nav__link">
      struct与class那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../union/" title="union那些事" class="md-nav__link">
      union那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../c_poly/" title="c实现C++多态那些事" class="md-nav__link">
      c实现C++多态那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../explicit/" title="explicit那些事" class="md-nav__link">
      explicit那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../friend/" title="friend那些事" class="md-nav__link">
      friend那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../using/" title="using那些事" class="md-nav__link">
      using那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../maohao/" title="::那些事" class="md-nav__link">
      ::那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../enum/" title="enum那些事" class="md-nav__link">
      enum那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../decltype/" title="decltype那些事" class="md-nav__link">
      decltype那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../pointer_refer/" title="引用与指针那些事" class="md-nav__link">
      引用与指针那些事
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../macro/" title="宏那些事" class="md-nav__link">
      宏那些事
    </a>
  </li>

        
      </ul>
    </nav>
  </li>

    
      
      
      


  <li class="md-nav__item md-nav__item--nested">
    
      <input class="md-toggle md-nav__toggle" data-md-toggle="nav-4" type="checkbox" id="nav-4">
    
    <label class="md-nav__link" for="nav-4">
      实战系列
    </label>
    <nav class="md-nav" data-md-component="collapsible" data-md-level="1">
      <label class="md-nav__title" for="nav-4">
        实战系列
      </label>
      <ul class="md-nav__list" data-md-scrollfix>
        
        
          
          
          


  <li class="md-nav__item">
    <a href="../../practical_exercises/10_day_practice/10_day/" title="10日狂练" class="md-nav__link">
      10日狂练
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../practical_exercises/key_exercises/key/" title="重点实战练习" class="md-nav__link">
      重点实战练习
    </a>
  </li>

        
      </ul>
    </nav>
  </li>

    
      
      
      


  <li class="md-nav__item md-nav__item--nested">
    
      <input class="md-toggle md-nav__toggle" data-md-toggle="nav-5" type="checkbox" id="nav-5">
    
    <label class="md-nav__link" for="nav-5">
      C++2.0新特性
    </label>
    <nav class="md-nav" data-md-component="collapsible" data-md-level="1">
      <label class="md-nav__title" for="nav-5">
        C++2.0新特性
      </label>
      <ul class="md-nav__list" data-md-scrollfix>
        
        
          
          
          


  <li class="md-nav__item">
    <a href="../../c%2B%2B2.0/c%2B%2B11/c%2B%2B11/" title="C++11" class="md-nav__link">
      C++11
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../update/" title="待更新" class="md-nav__link">
      待更新
    </a>
  </li>

        
      </ul>
    </nav>
  </li>

    
      
      
      


  <li class="md-nav__item md-nav__item--nested">
    
      <input class="md-toggle md-nav__toggle" data-md-toggle="nav-6" type="checkbox" id="nav-6">
    
    <label class="md-nav__link" for="nav-6">
      设计模式
    </label>
    <nav class="md-nav" data-md-component="collapsible" data-md-level="1">
      <label class="md-nav__title" for="nav-6">
        设计模式
      </label>
      <ul class="md-nav__list" data-md-scrollfix>
        
        
          
          
          


  <li class="md-nav__item">
    <a href="../../design_pattern/singleton/singleton/" title="单例模式" class="md-nav__link">
      单例模式
    </a>
  </li>

        
      </ul>
    </nav>
  </li>

    
      
      
      


  <li class="md-nav__item md-nav__item--nested">
    
      <input class="md-toggle md-nav__toggle" data-md-toggle="nav-7" type="checkbox" id="nav-7">
    
    <label class="md-nav__link" for="nav-7">
      源码剖析
    </label>
    <nav class="md-nav" data-md-component="collapsible" data-md-level="1">
      <label class="md-nav__title" for="nav-7">
        源码剖析
      </label>
      <ul class="md-nav__list" data-md-scrollfix>
        
        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/array/" title="array" class="md-nav__link">
      array
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/deque/" title="deque" class="md-nav__link">
      deque
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/queue_stack/" title="queue and stack" class="md-nav__link">
      queue and stack
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/list/" title="list" class="md-nav__link">
      list
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/vector/" title="vector" class="md-nav__link">
      vector
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/typename/" title="typename" class="md-nav__link">
      typename
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/traits/" title="traits" class="md-nav__link">
      traits
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/iterator/" title="iterator" class="md-nav__link">
      iterator
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/%E8%B0%88%E8%B0%88STL%E8%AE%BE%E8%AE%A1%E4%B9%8BEBO%E4%BC%98%E5%8C%96/" title="EBO优化" class="md-nav__link">
      EBO优化
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/rb_tree/" title="rb_tree" class="md-nav__link">
      rb_tree
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/set_multiset/" title="set and multiset" class="md-nav__link">
      set and multiset
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/map_multimap/" title="map and multimap" class="md-nav__link">
      map and multimap
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/hashtable/" title="hashtable" class="md-nav__link">
      hashtable
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/myhashtable/" title="myhashtable" class="md-nav__link">
      myhashtable
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../src_analysis/stl/unordered_map/" title="unordered_map" class="md-nav__link">
      unordered_map
    </a>
  </li>

        
      </ul>
    </nav>
  </li>

    
      
      
      


  <li class="md-nav__item md-nav__item--nested">
    
      <input class="md-toggle md-nav__toggle" data-md-toggle="nav-8" type="checkbox" id="nav-8">
    
    <label class="md-nav__link" for="nav-8">
      并发编程
    </label>
    <nav class="md-nav" data-md-component="collapsible" data-md-level="1">
      <label class="md-nav__title" for="nav-8">
        并发编程
      </label>
      <ul class="md-nav__list" data-md-scrollfix>
        
        
          
          
          


  <li class="md-nav__item">
    <a href="../../concurrency/concurrency_v1/concurrency/" title="C++ Concurrency in Action" class="md-nav__link">
      C++ Concurrency in Action
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../concurrency/Threading_In_CPlusPlus/thread/" title="Threading In C++" class="md-nav__link">
      Threading In C++
    </a>
  </li>

        
      </ul>
    </nav>
  </li>

    
      
      
      


  <li class="md-nav__item md-nav__item--nested">
    
      <input class="md-toggle md-nav__toggle" data-md-toggle="nav-9" type="checkbox" id="nav-9">
    
    <label class="md-nav__link" for="nav-9">
      惯用法
    </label>
    <nav class="md-nav" data-md-component="collapsible" data-md-level="1">
      <label class="md-nav__title" for="nav-9">
        惯用法
      </label>
      <ul class="md-nav__list" data-md-scrollfix>
        
        
          
          
          


  <li class="md-nav__item">
    <a href="../../codingStyleIdioms/classInitializers/" title="类初始化列表" class="md-nav__link">
      类初始化列表
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../codingStyleIdioms/enumclass/" title="枚举类替换命名空间" class="md-nav__link">
      枚举类替换命名空间
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../codingStyleIdioms/RAII/" title="RAII" class="md-nav__link">
      RAII
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../codingStyleIdioms/copy-swap/" title="copy and swap" class="md-nav__link">
      copy and swap
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../codingStyleIdioms/pImpl/" title="pImpl" class="md-nav__link">
      pImpl
    </a>
  </li>

        
      </ul>
    </nav>
  </li>

    
      
      
      


  <li class="md-nav__item md-nav__item--nested">
    
      <input class="md-toggle md-nav__toggle" data-md-toggle="nav-10" type="checkbox" id="nav-10">
    
    <label class="md-nav__link" for="nav-10">
      学习课程
    </label>
    <nav class="md-nav" data-md-component="collapsible" data-md-level="1">
      <label class="md-nav__title" for="nav-10">
        学习课程
      </label>
      <ul class="md-nav__list" data-md-scrollfix>
        
        
          
          
          


  <li class="md-nav__item">
    <a href="../../learn_class/modern_C%2B%2B_30/jiketime_class/" title="极客时间《现代C++实战30讲》" class="md-nav__link">
      极客时间《现代C++实战30讲》
    </a>
  </li>

        
      </ul>
    </nav>
  </li>

    
      
      
      


  <li class="md-nav__item md-nav__item--nested">
    
      <input class="md-toggle md-nav__toggle" data-md-toggle="nav-11" type="checkbox" id="nav-11">
    
    <label class="md-nav__link" for="nav-11">
      工具篇
    </label>
    <nav class="md-nav" data-md-component="collapsible" data-md-level="1">
      <label class="md-nav__title" for="nav-11">
        工具篇
      </label>
      <ul class="md-nav__list" data-md-scrollfix>
        
        
          
          
          


  <li class="md-nav__item">
    <a href="../../tool/output/" title="容器快捷输出工具" class="md-nav__link">
      容器快捷输出工具
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../tool/like_python/" title="像Python一样玩C/C++" class="md-nav__link">
      像Python一样玩C/C++
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../tool/look/" title="观察编译过程变化" class="md-nav__link">
      观察编译过程变化
    </a>
  </li>

        
          
          
          


  <li class="md-nav__item">
    <a href="../../tool/C%2B%2B%E7%9A%84Debug%E5%B7%A5%E5%85%B7dbg-macro/" title="C++的Debug工具dbg-macro" class="md-nav__link">
      C++的Debug工具dbg-macro
    </a>
  </li>

        
      </ul>
    </nav>
  </li>

    
      
      
      


  <li class="md-nav__item md-nav__item--nested">
    
      <input class="md-toggle md-nav__toggle" data-md-toggle="nav-12" type="checkbox" id="nav-12">
    
    <label class="md-nav__link" for="nav-12">
      拓展部分
    </label>
    <nav class="md-nav" data-md-component="collapsible" data-md-level="1">
      <label class="md-nav__title" for="nav-12">
        拓展部分
      </label>
      <ul class="md-nav__list" data-md-scrollfix>
        
        
          
          
          


  <li class="md-nav__item">
    <a href="../../extension/some_problem/string_int/" title="一些问题" class="md-nav__link">
      一些问题
    </a>
  </li>

        
      </ul>
    </nav>
  </li>

    
      
      
      


  <li class="md-nav__item">
    <a href="../../contribute/" title="项目贡献" class="md-nav__link">
      项目贡献
    </a>
  </li>

    
      
      
      


  <li class="md-nav__item">
    <a href="../../about/" title="联系作者" class="md-nav__link">
      联系作者
    </a>
  </li>

    
  </ul>
</nav>
                  </div>
                </div>
              </div>
            
            
              <div class="md-sidebar md-sidebar--secondary" data-md-component="toc">
                <div class="md-sidebar__scrollwrap">
                  <div class="md-sidebar__inner">
                    
<nav class="md-nav md-nav--secondary">
  
  
    
  
  
    <label class="md-nav__title" for="__toc">目录</label>
    <ul class="md-nav__list" data-md-scrollfix>
      
        <li class="md-nav__item">
  <a href="#1const" class="md-nav__link">
    1.const含义
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#2const" class="md-nav__link">
    2.const作用
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#3const" class="md-nav__link">
    3.const对象默认为文件局部变量
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#4" class="md-nav__link">
    4.定义常量
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#5const" class="md-nav__link">
    5.指针与const
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#6const" class="md-nav__link">
    6.函数中使用const
  </a>
  
</li>
      
        <li class="md-nav__item">
  <a href="#7const" class="md-nav__link">
    7.类中使用const
  </a>
  
</li>
      
      
      
      
      
    </ul>
  
</nav>
                  </div>
                </div>
              </div>
            
          
          <div class="md-content">
            <article class="md-content__inner md-typeset">
              
                
                
                <h1 id="const">const那些事<a class="headerlink" href="#const" title="Permanent link">&para;</a></h1>
<h2 id="1const">1.const含义<a class="headerlink" href="#1const" title="Permanent link">&para;</a></h2>
<p>常类型是指使用类型修饰符<strong>const</strong>说明的类型，常类型的变量或对象的值是不能被更新的。</p>
<h2 id="2const">2.const作用<a class="headerlink" href="#2const" title="Permanent link">&para;</a></h2>
<p>（1）可以定义常量</p>
<div class="codehilite"><pre><span></span><code><span class="k">const</span> <span class="kt">int</span> <span class="n">a</span><span class="o">=</span><span class="mi">100</span><span class="p">;</span>
</code></pre></div>


<p>（2）类型检查</p>
<p>const常量与#define宏定义常量的区别：~~<u><strong>const常量具有类型，编译器可以进行安全检查；#define宏定义没有数据类型，只是简单的字符串替换，不能进行安全检查。</strong></u>~~感谢两位大佬指出这里问题，见：</p>
<blockquote>
<p>https://github.com/Light-City/CPlusPlusThings/issues/5</p>
</blockquote>
<p><code>const</code> 定义的变量只有类型为整数或枚举，且以常量表达式初始化时才能作为常量表达式。其他情况下它只是一个 <code>const</code> 限定的变量，不要将与常量混淆。</p>
<p>（3）防止修改，起保护作用，增加程序健壮性</p>
<div class="codehilite"><pre><span></span><code><span class="kt">void</span> <span class="nf">f</span><span class="p">(</span><span class="k">const</span> <span class="kt">int</span> <span class="n">i</span><span class="p">){</span>
    <span class="n">i</span><span class="o">++</span><span class="p">;</span> <span class="c1">//error!</span>
<span class="p">}</span>
</code></pre></div>


<p>（4）可以节省空间，避免不必要的内存分配</p>
<p>const定义常量从汇编的角度来看，只是给出了对应的内存地址，而不是像#define一样给出的是立即数，所以，const定义的常量在程序运行过程中只有一份拷贝，而#define定义的常量在内存中有若干个拷贝。</p>
<h2 id="3const">3.const对象默认为文件局部变量<a class="headerlink" href="#3const" title="Permanent link">&para;</a></h2>
<p><font style="color:red">注意：非const变量默认为extern。要使const变量能够在其他文件中访问，必须在文件中显式地指定它为extern。</font></p>

<blockquote>
<p>未被const修饰的变量在不同文件的访问</p>
</blockquote>
<div class="codehilite"><pre><span></span><code><span class="c1">// file1.cpp</span>
<span class="kt">int</span> <span class="n">ext</span>
<span class="c1">// file2.cpp</span>
<span class="cp">#include</span><span class="cpf">&lt;iostream&gt;</span><span class="cp"></span>
<span class="cm">/**</span>
<span class="cm"> * by 光城</span>
<span class="cm"> * compile: g++ -o file file2.cpp file1.cpp</span>
<span class="cm"> * execute: ./file</span>
<span class="cm"> */</span>
<span class="k">extern</span> <span class="kt">int</span> <span class="n">ext</span><span class="p">;</span>
<span class="kt">int</span> <span class="nf">main</span><span class="p">(){</span>
    <span class="n">std</span><span class="o">::</span><span class="n">cout</span><span class="o">&lt;&lt;</span><span class="p">(</span><span class="n">ext</span><span class="o">+</span><span class="mi">10</span><span class="p">)</span><span class="o">&lt;&lt;</span><span class="n">std</span><span class="o">::</span><span class="n">endl</span><span class="p">;</span>
<span class="p">}</span>
</code></pre></div>


<blockquote>
<p>const常量在不同文件的访问</p>
</blockquote>
<div class="codehilite"><pre><span></span><code><span class="c1">//extern_file1.cpp</span>
<span class="k">extern</span> <span class="k">const</span> <span class="kt">int</span> <span class="n">ext</span><span class="o">=</span><span class="mi">12</span><span class="p">;</span>
<span class="c1">//extern_file2.cpp</span>
<span class="cp">#include</span><span class="cpf">&lt;iostream&gt;</span><span class="cp"></span>
<span class="cm">/**</span>
<span class="cm"> * by 光城</span>
<span class="cm"> * compile: g++ -o file const_file2.cpp const_file1.cpp</span>
<span class="cm"> * execute: ./file</span>
<span class="cm"> */</span>
<span class="k">extern</span> <span class="k">const</span> <span class="kt">int</span> <span class="n">ext</span><span class="p">;</span>
<span class="kt">int</span> <span class="nf">main</span><span class="p">(){</span>
    <span class="n">std</span><span class="o">::</span><span class="n">cout</span><span class="o">&lt;&lt;</span><span class="n">ext</span><span class="o">&lt;&lt;</span><span class="n">std</span><span class="o">::</span><span class="n">endl</span><span class="p">;</span>
<span class="p">}</span>
</code></pre></div>


<p><font style="color:red">小结：可以发现未被const修饰的变量不需要extern显式声明！而const常量需要显式声明extern，并且需要做初始化！因为常量在定义后就不能被修改，所以定义时必须初始化。</font></p>

<h2 id="4">4.定义常量<a class="headerlink" href="#4" title="Permanent link">&para;</a></h2>
<div class="codehilite"><pre><span></span><code><span class="k">const</span> <span class="kt">int</span> <span class="n">b</span> <span class="o">=</span> <span class="mi">10</span><span class="p">;</span>
<span class="n">b</span> <span class="o">=</span> <span class="mi">0</span><span class="p">;</span> <span class="c1">// error: assignment of read-only variable ‘b’</span>
<span class="k">const</span> <span class="n">string</span> <span class="n">s</span> <span class="o">=</span> <span class="s">&quot;helloworld&quot;</span><span class="p">;</span>
<span class="k">const</span> <span class="kt">int</span> <span class="n">i</span><span class="p">,</span><span class="n">j</span><span class="o">=</span><span class="mi">0</span> <span class="c1">// error: uninitialized const ‘i’</span>
</code></pre></div>


<p>上述有两个错误，第一：b为常量，不可更改！第二：i为常量，必须进行初始化！(因为常量在定义后就不能被修改，所以定义时必须初始化。)</p>
<h2 id="5const">5.指针与const<a class="headerlink" href="#5const" title="Permanent link">&para;</a></h2>
<p>与指针相关的const有四种：</p>
<div class="codehilite"><pre><span></span><code><span class="k">const</span> <span class="kt">char</span> <span class="o">*</span> <span class="n">a</span><span class="p">;</span> <span class="c1">//指向const对象的指针或者说指向常量的指针。</span>
<span class="kt">char</span> <span class="k">const</span> <span class="o">*</span> <span class="n">a</span><span class="p">;</span> <span class="c1">//同上</span>
<span class="kt">char</span> <span class="o">*</span> <span class="k">const</span> <span class="n">a</span><span class="p">;</span> <span class="c1">//指向类型对象的const指针。或者说常指针、const指针。</span>
<span class="k">const</span> <span class="kt">char</span> <span class="o">*</span> <span class="k">const</span> <span class="n">a</span><span class="p">;</span> <span class="c1">//指向const对象的const指针。</span>
</code></pre></div>


<p>小结：如果<em>const</em>位于<code>*</code>的左侧，则const就是用来修饰指针所指向的变量，即指针指向为常量；如果const位于<code>*</code>的右侧，<em>const</em>就是修饰指针本身，即指针本身是常量。</p>
<p>具体使用如下：</p>
<p>（1）指向常量的指针</p>
<div class="codehilite"><pre><span></span><code><span class="k">const</span> <span class="kt">int</span> <span class="o">*</span><span class="n">ptr</span><span class="p">;</span>
<span class="o">*</span><span class="n">ptr</span> <span class="o">=</span> <span class="mi">10</span><span class="p">;</span> <span class="c1">//error</span>
</code></pre></div>


<p>ptr是一个指向int类型const对象的指针，const定义的是int类型，也就是ptr所指向的对象类型，而不是ptr本身，所以ptr可以不用赋初始值。但是不能通过ptr去修改所指对象的值。</p>
<p>除此之外，也不能使用void<code>*</code>指针保存const对象的地址，必须使用const void<code>*</code>类型的指针保存const对象的地址。</p>
<div class="codehilite"><pre><span></span><code><span class="k">const</span> <span class="kt">int</span> <span class="n">p</span> <span class="o">=</span> <span class="mi">10</span><span class="p">;</span>
<span class="k">const</span> <span class="kt">void</span> <span class="o">*</span> <span class="n">vp</span> <span class="o">=</span> <span class="o">&amp;</span><span class="n">p</span><span class="p">;</span>
<span class="kt">void</span> <span class="o">*</span><span class="n">vp</span> <span class="o">=</span> <span class="o">&amp;</span><span class="n">p</span><span class="p">;</span> <span class="c1">//error</span>
</code></pre></div>


<p>另外一个重点是：<strong>允许把非const对象的地址赋给指向const对象的指针</strong>。</p>
<p>将非const对象的地址赋给const对象的指针:</p>
<div class="codehilite"><pre><span></span><code><span class="k">const</span> <span class="kt">int</span> <span class="o">*</span><span class="n">ptr</span><span class="p">;</span>
<span class="kt">int</span> <span class="n">val</span> <span class="o">=</span> <span class="mi">3</span><span class="p">;</span>
<span class="n">ptr</span> <span class="o">=</span> <span class="o">&amp;</span><span class="n">val</span><span class="p">;</span> <span class="c1">//ok</span>
</code></pre></div>


<p>我们不能通过ptr指针来修改val的值，即使它指向的是非const对象!</p>
<p>我们不能使用指向const对象的指针修改基础对象，然而如果该指针指向了非const对象，可用其他方式修改其所指的对象。可以修改const指针所指向的值的，但是不能通过const对象指针来进行而已！如下修改：</p>
<div class="codehilite"><pre><span></span><code><span class="kt">int</span> <span class="o">*</span><span class="n">ptr1</span> <span class="o">=</span> <span class="o">&amp;</span><span class="n">val</span><span class="p">;</span>
<span class="o">*</span><span class="n">ptr1</span><span class="o">=</span><span class="mi">4</span><span class="p">;</span>
<span class="n">cout</span><span class="o">&lt;&lt;*</span><span class="n">ptr</span><span class="o">&lt;&lt;</span><span class="n">endl</span><span class="p">;</span>
</code></pre></div>


<p><font style="color:red">小结：对于指向常量的指针，不能通过指针来修改对象的值。<br/>也不能使用void`*`指针保存const对象的地址，必须使用const void`*`类型的指针保存const对象的地址。<br/>允许把非const对象的地址赋值给const对象的指针，如果要修改指针所指向的对象值，必须通过其他方式修改，不能直接通过当前指针直接修改。</font></p>

<p>（2）常指针</p>
<p>const指针必须进行初始化，且const指针的值不能修改。</p>
<div class="codehilite"><pre><span></span><code><span class="cp">#include</span><span class="cpf">&lt;iostream&gt;</span><span class="cp"></span>
<span class="k">using</span> <span class="k">namespace</span> <span class="n">std</span><span class="p">;</span>
<span class="kt">int</span> <span class="nf">main</span><span class="p">(){</span>

    <span class="kt">int</span> <span class="n">num</span><span class="o">=</span><span class="mi">0</span><span class="p">;</span>
    <span class="kt">int</span> <span class="o">*</span> <span class="k">const</span> <span class="n">ptr</span><span class="o">=&amp;</span><span class="n">num</span><span class="p">;</span> <span class="c1">//const指针必须初始化！且const指针的值不能修改</span>
    <span class="kt">int</span> <span class="o">*</span> <span class="n">t</span> <span class="o">=</span> <span class="o">&amp;</span><span class="n">num</span><span class="p">;</span>
    <span class="o">*</span><span class="n">t</span> <span class="o">=</span> <span class="mi">1</span><span class="p">;</span>
    <span class="n">cout</span><span class="o">&lt;&lt;*</span><span class="n">ptr</span><span class="o">&lt;&lt;</span><span class="n">endl</span><span class="p">;</span>
<span class="p">}</span>
</code></pre></div>


<p>上述修改ptr指针所指向的值，可以通过非const指针来修改。</p>
<p>最后，当把一个const常量的地址赋值给ptr时候，由于ptr指向的是一个变量，而不是const常量，所以会报错，出现：const int<code>*</code> -&gt; int <code>*</code>错误！</p>
<div class="codehilite"><pre><span></span><code><span class="cp">#include</span><span class="cpf">&lt;iostream&gt;</span><span class="cp"></span>
<span class="k">using</span> <span class="k">namespace</span> <span class="n">std</span><span class="p">;</span>
<span class="kt">int</span> <span class="nf">main</span><span class="p">(){</span>
    <span class="k">const</span> <span class="kt">int</span> <span class="n">num</span><span class="o">=</span><span class="mi">0</span><span class="p">;</span>
    <span class="kt">int</span> <span class="o">*</span> <span class="k">const</span> <span class="n">ptr</span><span class="o">=&amp;</span><span class="n">num</span><span class="p">;</span> <span class="c1">//error! const int* -&gt; int*</span>
    <span class="n">cout</span><span class="o">&lt;&lt;*</span><span class="n">ptr</span><span class="o">&lt;&lt;</span><span class="n">endl</span><span class="p">;</span>
<span class="p">}</span>
</code></pre></div>


<p>上述若改为 const int <code>*</code>ptr或者改为const int <code>*</code>const ptr，都可以正常！</p>
<p>（3）指向常量的常指针</p>
<p>理解完前两种情况，下面这个情况就比较好理解了：</p>
<div class="codehilite"><pre><span></span><code><span class="k">const</span> <span class="kt">int</span> <span class="n">p</span> <span class="o">=</span> <span class="mi">3</span><span class="p">;</span>
<span class="k">const</span> <span class="kt">int</span> <span class="o">*</span> <span class="k">const</span> <span class="n">ptr</span> <span class="o">=</span> <span class="o">&amp;</span><span class="n">p</span><span class="p">;</span> 
</code></pre></div>


<p>ptr是一个const指针，然后指向了一个int 类型的const对象。</p>
<h2 id="6const">6.函数中使用const<a class="headerlink" href="#6const" title="Permanent link">&para;</a></h2>
<blockquote>
<p>cost修饰函数返回值</p>
</blockquote>
<p>这个跟const修饰普通变量以及指针的含义基本相同：</p>
<p>（1）const int</p>
<div class="codehilite"><pre><span></span><code><span class="k">const</span> <span class="kt">int</span> <span class="nf">func1</span><span class="p">();</span>
</code></pre></div>


<p>这个本身无意义，因为参数返回本身就是赋值给其他的变量！</p>
<p>（2）const int*</p>
<div class="codehilite"><pre><span></span><code><span class="k">const</span> <span class="kt">int</span><span class="o">*</span> <span class="nf">func2</span><span class="p">();</span>
</code></pre></div>


<p>指针指向的内容不变。</p>
<p>（3）int *const</p>
<div class="codehilite"><pre><span></span><code><span class="kt">int</span> <span class="o">*</span><span class="k">const</span> <span class="nf">func2</span><span class="p">();</span>
</code></pre></div>


<p>指针本身不可变。</p>
<blockquote>
<p>const修饰函数参数</p>
</blockquote>
<p>（1）传递过来的参数及指针本身在函数内不可变，无意义！</p>
<div class="codehilite"><pre><span></span><code><span class="kt">void</span> <span class="nf">func</span><span class="p">(</span><span class="k">const</span> <span class="kt">int</span> <span class="n">var</span><span class="p">);</span> <span class="c1">// 传递过来的参数不可变</span>
<span class="kt">void</span> <span class="nf">func</span><span class="p">(</span><span class="kt">int</span> <span class="o">*</span><span class="k">const</span> <span class="n">var</span><span class="p">);</span> <span class="c1">// 指针本身不可变</span>
</code></pre></div>


<p>表明参数在函数体内不能被修改，但此处没有任何意义，var本身就是形参，在函数内不会改变。包括传入的形参是指针也是一样。</p>
<p>输入参数采用“值传递”，由于函数将自动产生临时变量用于复制该参数，该输入参数本来就无需保护，所以不要加const 修饰。</p>
<p>（2）参数指针所指内容为常量不可变</p>
<div class="codehilite"><pre><span></span><code><span class="kt">void</span> <span class="nf">StringCopy</span><span class="p">(</span><span class="kt">char</span> <span class="o">*</span><span class="n">dst</span><span class="p">,</span> <span class="k">const</span> <span class="kt">char</span> <span class="o">*</span><span class="n">src</span><span class="p">);</span>
</code></pre></div>


<p>其中src 是输入参数，dst 是输出参数。给src加上const修饰后，如果函数体内的语句试图改动src的内容，编译器将指出错误。这就是加了const的作用之一。</p>
<p>（3）参数为引用，为了增加效率同时防止修改。</p>
<div class="codehilite"><pre><span></span><code><span class="kt">void</span> <span class="n">func</span><span class="p">(</span><span class="k">const</span> <span class="n">A</span> <span class="o">&amp;</span><span class="n">a</span><span class="p">)</span>
</code></pre></div>


<p>对于非内部数据类型的参数而言，象void func(A a) 这样声明的函数注定效率比较低。因为函数体内将产生A 类型</p>
<p>的临时对象用于复制参数a，而临时对象的构造、复制、析构过程都将消耗时间。</p>
<p>为了提高效率，可以将函数声明改为void func(A &amp;a)，因为“引用传递”仅借用一下参数的别名而已，不需要产生临</p>
<p>时对象。但是函数void func(A &amp;a) 存在一个缺点：</p>
<p>“引用传递”有可能改变参数a，这是我们不期望的。解决这个问题很容易，加const修饰即可，因此函数最终成为</p>
<p>void func(const A &amp;a)。</p>
<p>以此类推，是否应将void func(int x) 改写为void func(const int &amp;x)，以便提高效率？完全没有必要，因为内部数</p>
<p>据类型的参数不存在构造、析构的过程，而复制也非常快，“值传递”和“引用传递”的效率几乎相当。</p>
<p><font style="color:red">小结：对于非内部数据类型的输入参数，应该将“值传递”的方式改为“const 引用传递”，目的是提高效率。例如将void func(A a) 改为void func(const A &a)。<br/>对于内部数据类型的输入参数，不要将“值传递”的方式改为“const 引用传递”。否则既达不到提高效率的目的，又降低了函数的可理解性。例如void func(int x) 不应该改为void func(const int &x)。</font></p>

<p>以上解决了两个面试问题：</p>
<p>（1）如果函数需要传入一个指针，是否需要为该指针加上const，把const加在指针不同的位置有什么区别；</p>
<p>（2）如果写的函数需要传入的参数是一个复杂类型的实例，传入值参数或者引用参数有什么区别，什么时候需要为传入的引用参数加上const。 </p>
<h2 id="7const">7.类中使用const<a class="headerlink" href="#7const" title="Permanent link">&para;</a></h2>
<p>在一个类中，任何不会修改数据成员的函数都应该声明为const类型。如果在编写const成员函数时，不慎修改</p>
<p>数据成员，或者调用了其它非const成员函数，编译器将指出错误，这无疑会提高程序的健壮性。使用const关</p>
<p>字进行说明的成员函数，称为常成员函数。只有常成员函数才有资格操作常量或常对象，没有使用const关键字</p>
<p>明的成员函数不能用来操作常对象。</p>
<p>对于类中的const成员变量必须通过初始化列表进行初始化，如下所示：</p>
<div class="codehilite"><pre><span></span><code><span class="k">class</span> <span class="nc">Apple</span>
<span class="p">{</span>
<span class="k">private</span><span class="o">:</span>
    <span class="kt">int</span> <span class="n">people</span><span class="p">[</span><span class="mi">100</span><span class="p">];</span>
<span class="k">public</span><span class="o">:</span>
    <span class="n">Apple</span><span class="p">(</span><span class="kt">int</span> <span class="n">i</span><span class="p">);</span> 
    <span class="k">const</span> <span class="kt">int</span> <span class="n">apple_number</span><span class="p">;</span>
<span class="p">};</span>

<span class="n">Apple</span><span class="o">::</span><span class="n">Apple</span><span class="p">(</span><span class="kt">int</span> <span class="n">i</span><span class="p">)</span><span class="o">:</span><span class="n">apple_number</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
<span class="p">{</span>

<span class="p">}</span>
</code></pre></div>


<p>const对象只能访问const成员函数,而非const对象可以访问任意的成员函数,包括const成员函数.</p>
<p>例如：</p>
<div class="codehilite"><pre><span></span><code><span class="c1">//apple.cpp</span>
<span class="k">class</span> <span class="nc">Apple</span>
<span class="p">{</span>
<span class="k">private</span><span class="o">:</span>
    <span class="kt">int</span> <span class="n">people</span><span class="p">[</span><span class="mi">100</span><span class="p">];</span>
<span class="k">public</span><span class="o">:</span>
    <span class="n">Apple</span><span class="p">(</span><span class="kt">int</span> <span class="n">i</span><span class="p">);</span> 
    <span class="k">const</span> <span class="kt">int</span> <span class="n">apple_number</span><span class="p">;</span>
    <span class="kt">void</span> <span class="nf">take</span><span class="p">(</span><span class="kt">int</span> <span class="n">num</span><span class="p">)</span> <span class="k">const</span><span class="p">;</span>
    <span class="kt">int</span> <span class="nf">add</span><span class="p">(</span><span class="kt">int</span> <span class="n">num</span><span class="p">);</span>
    <span class="kt">int</span> <span class="nf">add</span><span class="p">(</span><span class="kt">int</span> <span class="n">num</span><span class="p">)</span> <span class="k">const</span><span class="p">;</span>
    <span class="kt">int</span> <span class="nf">getCount</span><span class="p">()</span> <span class="k">const</span><span class="p">;</span>

<span class="p">};</span>
<span class="c1">//main.cpp</span>
<span class="cp">#include</span><span class="cpf">&lt;iostream&gt;</span><span class="cp"></span>
<span class="cp">#include</span><span class="cpf">&quot;apple.cpp&quot;</span><span class="cp"></span>
<span class="k">using</span> <span class="k">namespace</span> <span class="n">std</span><span class="p">;</span>

<span class="n">Apple</span><span class="o">::</span><span class="n">Apple</span><span class="p">(</span><span class="kt">int</span> <span class="n">i</span><span class="p">)</span><span class="o">:</span><span class="n">apple_number</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
<span class="p">{</span>

<span class="p">}</span>
<span class="kt">int</span> <span class="n">Apple</span><span class="o">::</span><span class="n">add</span><span class="p">(</span><span class="kt">int</span> <span class="n">num</span><span class="p">){</span>
    <span class="n">take</span><span class="p">(</span><span class="n">num</span><span class="p">);</span>
<span class="p">}</span>
<span class="kt">int</span> <span class="n">Apple</span><span class="o">::</span><span class="n">add</span><span class="p">(</span><span class="kt">int</span> <span class="n">num</span><span class="p">)</span> <span class="k">const</span><span class="p">{</span>
    <span class="n">take</span><span class="p">(</span><span class="n">num</span><span class="p">);</span>
<span class="p">}</span>
<span class="kt">void</span> <span class="n">Apple</span><span class="o">::</span><span class="n">take</span><span class="p">(</span><span class="kt">int</span> <span class="n">num</span><span class="p">)</span> <span class="k">const</span>
<span class="p">{</span>
    <span class="n">cout</span><span class="o">&lt;&lt;</span><span class="s">&quot;take func &quot;</span><span class="o">&lt;&lt;</span><span class="n">num</span><span class="o">&lt;&lt;</span><span class="n">endl</span><span class="p">;</span>
<span class="p">}</span>
<span class="kt">int</span> <span class="n">Apple</span><span class="o">::</span><span class="n">getCount</span><span class="p">()</span> <span class="k">const</span>
<span class="p">{</span>
    <span class="n">take</span><span class="p">(</span><span class="mi">1</span><span class="p">);</span>
<span class="c1">//    add(); //error</span>
    <span class="k">return</span> <span class="n">apple_number</span><span class="p">;</span>
<span class="p">}</span>
<span class="kt">int</span> <span class="n">main</span><span class="p">(){</span>
    <span class="n">Apple</span> <span class="n">a</span><span class="p">(</span><span class="mi">2</span><span class="p">);</span>
    <span class="n">cout</span><span class="o">&lt;&lt;</span><span class="n">a</span><span class="p">.</span><span class="n">getCount</span><span class="p">()</span><span class="o">&lt;&lt;</span><span class="n">endl</span><span class="p">;</span>
    <span class="n">a</span><span class="p">.</span><span class="n">add</span><span class="p">(</span><span class="mi">10</span><span class="p">);</span>
    <span class="k">const</span> <span class="n">Apple</span> <span class="nf">b</span><span class="p">(</span><span class="mi">3</span><span class="p">);</span>
    <span class="n">b</span><span class="p">.</span><span class="n">add</span><span class="p">(</span><span class="mi">100</span><span class="p">);</span>
    <span class="k">return</span> <span class="mi">0</span><span class="p">;</span>
<span class="p">}</span>
<span class="c1">//编译： g++ -o main main.cpp apple.cpp</span>
<span class="c1">//结果</span>
<span class="n">take</span> <span class="n">func</span> <span class="mi">1</span>
<span class="mi">2</span>
<span class="n">take</span> <span class="n">func</span> <span class="mi">10</span>
<span class="n">take</span> <span class="n">func</span> <span class="mi">100</span>
</code></pre></div>


<p>上面getCount()方法中调用了一个add方法，而add方法并非const修饰，所以运行报错。也就是说const对象只能访问const成员函数。</p>
<p>而add方法又调用了const修饰的take方法，证明了非const对象可以访问任意的成员函数,包括const成员函数。</p>
<p>除此之外，我们也看到add的一个重载函数，也输出了两个结果，说明const对象默认调用const成员函数。</p>
<p>我们除了上述的初始化const常量用初始化列表方式外，也可以通过下面方法：</p>
<p>第一：将常量定义与static结合，也就是：</p>
<div class="codehilite"><pre><span></span><code><span class="k">static</span> <span class="k">const</span> <span class="kt">int</span> <span class="n">apple_number</span>
</code></pre></div>


<p>第二：在外面初始化：</p>
<div class="codehilite"><pre><span></span><code><span class="k">const</span> <span class="kt">int</span> <span class="n">Apple</span><span class="o">::</span><span class="n">apple_number</span><span class="o">=</span><span class="mi">10</span><span class="p">;</span>
</code></pre></div>


<p>当然，如果你使用c++11进行编译，直接可以在定义出初始化，可以直接写成：</p>
<div class="codehilite"><pre><span></span><code><span class="k">static</span> <span class="k">const</span> <span class="kt">int</span> <span class="n">apple_number</span><span class="o">=</span><span class="mi">10</span><span class="p">;</span>
<span class="err">或者</span>
<span class="k">const</span> <span class="kt">int</span> <span class="n">apple_number</span><span class="o">=</span><span class="mi">10</span><span class="p">;</span>
</code></pre></div>


<p>这两种都在c++11中支持！</p>
<p>编译的时候加上<code>-std=c++11</code>即可！</p>
<p>这里提到了static，下面简单的说一下：</p>
<p>在C++中，static静态成员变量不能在类的内部初始化。在类的内部只是声明，定义必须在类定义体的外部，通常在类的实现文件中初始化。</p>
<p>在类中声明：</p>
<div class="codehilite"><pre><span></span><code><span class="k">static</span> <span class="kt">int</span> <span class="n">ap</span><span class="p">;</span>
</code></pre></div>


<p>在类实现文件中使用：</p>
<div class="codehilite"><pre><span></span><code><span class="kt">int</span> <span class="n">Apple</span><span class="o">::</span><span class="n">ap</span><span class="o">=</span><span class="mi">666</span>
</code></pre></div>


<p>对于此项，c++11不能进行声明并初始化，也就是上述使用方法。</p>
                
                  
                
                
              
              
                


              
            </article>
          </div>
        </div>
      </main>
      
        
<footer class="md-footer">
  
    <div class="md-footer-nav">
      <nav class="md-footer-nav__inner md-grid">
        
          <a href="../../use/" title="使用须知" class="md-flex md-footer-nav__link md-footer-nav__link--prev" rel="prev">
            <div class="md-flex__cell md-flex__cell--shrink">
              <i class="md-icon md-icon--arrow-back md-footer-nav__button"></i>
            </div>
            <div class="md-flex__cell md-flex__cell--stretch md-footer-nav__title">
              <span class="md-flex__ellipsis">
                <span class="md-footer-nav__direction">
                  上一页
                </span>
                使用须知
              </span>
            </div>
          </a>
        
        
          <a href="../static/" title="static那些事" class="md-flex md-footer-nav__link md-footer-nav__link--next" rel="next">
            <div class="md-flex__cell md-flex__cell--stretch md-footer-nav__title">
              <span class="md-flex__ellipsis">
                <span class="md-footer-nav__direction">
                  下一页
                </span>
                static那些事
              </span>
            </div>
            <div class="md-flex__cell md-flex__cell--shrink">
              <i class="md-icon md-icon--arrow-forward md-footer-nav__button"></i>
            </div>
          </a>
        
      </nav>
    </div>
  
  <div class="md-footer-meta md-typeset">
    <div class="md-footer-meta__inner md-grid">
      <div class="md-footer-copyright">
        
          <div class="md-footer-copyright__highlight">
            Copyright &copy; 2020 - 2020 光城
          </div>
        
        powered by
        <a href="https://www.mkdocs.org" target="_blank" rel="noopener">MkDocs</a>
        and
        <a href="https://squidfunk.github.io/mkdocs-material/" target="_blank" rel="noopener">
          Material for MkDocs</a>
      </div>
      
  <div class="md-footer-social">
    <link rel="stylesheet" href="../../assets/fonts/font-awesome.css">
    
      <a href="https://github.com/Light-City/CPlusPlusThings" target="_blank" rel="noopener" title="github" class="md-footer-social__link fa fa-github"></a>
    
  </div>

    </div>
  </div>
</footer>
      
    </div>
    
      <script src="../../assets/javascripts/application.c33a9706.js"></script>
      
        
        
          
          <script src="../../assets/javascripts/lunr/lunr.stemmer.support.js"></script>
          
            
              
                <script src="../../assets/javascripts/lunr/tinyseg.js"></script>
              
              
                <script src="../../assets/javascripts/lunr/lunr.ja.js"></script>
              
            
          
          
        
      
      <script>app.initialize({version:"1.1",url:{base:"../.."}})</script>
      
    
  </body>
</html>
