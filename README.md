# Dango_static_media_config

# in settings.py of project 

      STATIC_URL = '/static/'
      MEDIA_URL = '/media/'
      STATICFILES_DIRS = [
          os.path.join(BASE_DIR,'static')
      ]
      STATIC_ROOT= os.path.join(BASE_DIR, '../static_cdn')
      MEDIA_ROOT= os.path.join(BASE_DIR, '../media_cdn')
 
 # in urls.py of project 
 
      from django.conf import settings
      from django.conf.urls.static import static
      
      
      
      
      
      
      if settings.DEBUG :
          urlpatterns += static(settings.MEDIA_URL, document_root = settings.MEDIA_ROOT)
          urlpatterns += static(settings.STATIC_URL, document_root = settings.STATIC_ROOT)
