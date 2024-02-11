# Hibernar - Arquitectura
------------------------------------------
https://www.tutorialspoint.com/hibernate/hibernate_architecture.htm

Hibernate tiene una arquitectura en capas que ayuda al usuario a operar sin tener que conocer las API subyacentes. Hibernate utiliza la base de datos y los datos de configuración para proporcionar servicios de persistencia (y objetos persistentes) a la aplicación.

## Conexión mediante JDBC, Hibernate a base de datos H2, la Java SQL database.
------------------------------------------------------------------------------
https://stackoverflow.com/questions/3807503/what-is-the-purpose-of-two-config-files-for-hibernate/3808406#3808406

Si está utilizando la API patentada de Hibernate, necesitará hibernate.cfg.xml. Si está utilizando JPA, es decir, Hibernate EntityManager, necesitará persistence.xml.

Por lo tanto, generalmente no necesita ambos, ya que utiliza la API patentada de Hibernate o JPA.

Sin embargo, si estaba utilizando la API patentada de Hibernate y ya tiene hibernate.cfg.xml (y archivos de mapeo XML hbm.xml) pero desea comenzar a usar JPA, puede reutilizar los archivos de configuración existentes haciendo referencia a hibernate.cfg.xml en el persistence.xml en la propiedad hibernate.ejb.cfgfile y, por lo tanto, tendrá ambos archivos. Reutilizar archivos hbm.xml existentes es, en mi opinión, un escenario realista que podría justificar conservar ambos (incluso si probablemente migraría a anotaciones JPA a largo plazo).

***
Nota: Si utiliza 'Hibernate.cfg.xml' la conexión es mediante 'SessionFactory' o 
      si utiliza 'persistence.xml' la conexion es mediante 'EntityManagerFactory'
***
