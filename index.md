---
layout: index
lang: tr
permalink: /
---

<!--
Start About Section
==================================== -->
<section class="about-2 section bg-gray" style="padding-top: 30px;" id="about">
    <div class="container">
        <div class="row">
            <div class="col-12 col-md-5">
                <h2>Almanya Yüksekokulları Mezunlar Derneği (AYMED)</h2>
            </div>
            <div class="col-12 col-md-7">
                <p>Almanya Yüksekokulları Mezunlar Derneği (AYMED), merkezi İstanbulda olup, Almanyada yüksek eğitim görerek Türkiyeye dönen bir grup insiyatif sahibi mezun tarafından 1991 yılında kurulmuştur.
                </p>
                <p>
                Derneğin amacı, Almanyada yüksek eğitim görerek Türkiyeye dönen mezunların, Türkiyenin iş ve sosyal ortamına uyum sağlamalarına yardımcı olmak, beraberlerinde getirdikleri teknolojik gelişmeleri, bilgi birikimlerini Türkiyenin iş, sanayi ve ekonomi hayatına yararlı olacak şekilde kullanımını sağlamaktır.</p>
            </div>
        </div> 		<!-- End row -->
    </div>   	<!-- End container -->
</section>   <!-- End section -->

<section class="articles">
    <div class="container">
        <div class="row">
            <div class="col-lg-4 col-md-6 d-flex align-items-stretch">
                <div class="card m-2 h-100">
                <!-- <img class="card-img-top" src="" alt=""> -->
                    <div class="card-header">
                        <div class="d-flex align-items-center">
                            <h5 class="mx-auto w-100">Haberler</h5>
                            <i class="fa-solid fa-newspaper fa-2x ml-auto header-icon"></i>
                        </div>
                    </div>
                    <div class="card-body">
                        <!-- <ul> -->
                        {% assign haberler = site.haberler | where:"lang", page.lang | sort: 'date' | reverse %}
                        {% for haber in haberler limit:5 %}
                        <div class="d-flex align-items-stretch pb-2">
                            <div><i class="bx bx-chevron-right chevron-large"></i></div>
                            <div class="article">
                                <div>
                                <a href="{{ site.baseurl }}{{ haber.permalink }}">{{ haber.title }}</a>
                                </div>
                                <div class="small">
                                <span class="small text-muted text"><em>{{ haber.date | date: "%Y-%m-%d" }}</em></span> -
                                {{ haber.short_description }}
                                </div>
                            </div>
                        </div>
                        {% endfor %}
                    </div>
                    <div class="card-footer text-center">
                        <a href="{{ site.baseurl }}/tr/haberler/aymed-den" class="card-link"><i class="fas fa-arrow mb-2"></i> Tüm Haberler</a>
                    </div>
                </div>
            </div>
            <div class="col-lg-4 col-md-6 d-flex align-items-stretch">
                <div class="card m-2 h-100">
                <!-- <img class="card-img-top" src="" alt=""> -->
                    <div class="card-header">
                        <div class="d-flex align-items-center">
                            <h5 class="mx-auto w-100">Duyurular</h5>
                            <i class="fa-solid fa-circle-info fa-2x ml-auto header-icon"></i>
                        </div>
                    </div>
                    <div class="card-body">
                        <!-- <ul> -->
                        {% assign duyurular = site.duyurular | where:"lang", page.lang | sort: 'date' | reverse %}
                        {% for duyuru in duyurular limit:5 %}
                        <div class="d-flex align-items-stretch pb-2">
                            <div><i class="bx bx-chevron-right chevron-large"></i></div>
                            <div class="article">
                                <div>
                                <a href="{{ site.baseurl }}{{ duyuru.permalink }}">{{ duyuru.title }}</a>
                                </div>
                                <div class="small">
                                <span class="small text-muted text"><em>{{ duyuru.date | date: "%Y-%m-%d" }}</em></span> -
                                {{ duyuru.short_description }}
                                </div>
                            </div>
                        </div>
                        {% endfor %}
                        <!-- </ul> -->
                    </div>
                    <div class="card-footer text-center">
                        <a href="{{ site.baseurl }}/tr/duyurular" class="card-link"><i class="fas fa-arrow mb-2"></i> Tüm Duyurular</a>
                    </div>
                </div>
            </div>
            <div class="col-lg-4 col-md-6 d-flex align-items-stretch">
                <div class="card m-2 h-100">
                <!-- <img class="card-img-top" src="" alt=""> -->
                    <div class="card-header">
                        <div class="d-flex align-items-center">
                            <h5 class="mx-auto w-100">Etkinlikler</h5>
                            <i class="fa-solid fa-users fa-2x ml-auto header-icon"></i>
                        </div>
                    </div>
                    <div class="card-body">
                        <!-- <ul> -->
                        {% assign etkinlikler = site.etkinlikler | where:"lang", page.lang | sort: 'date' | reverse %}
                        {% for etkinlik in etkinlikler limit:5 %}
                        <div class="d-flex align-items-stretch pb-2">
                            <div><i class="bx bx-chevron-right chevron-large"></i></div>
                            <div class="article">
                                <div>
                                <a href="{{ site.baseurl }}{{ etkinlik.permalink }}">{{ etkinlik.title }}</a>
                                </div>
                                <div class="small">
                                <span class="small text-muted text"><em>{{ etkinlik.date | date: "%Y-%m-%d" }}</em></span> -
                                {{ etkinlik.short_description }}
                                </div>
                            </div>
                        </div>
                        {% endfor %}
                    </div>
                    <div class="card-footer text-center">
                        <a href="{{ site.baseurl }}/tr/etkinlikler" class="card-link"><i class="fas fa-arrow mb-2"></i> Tüm Etkinlikler</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>