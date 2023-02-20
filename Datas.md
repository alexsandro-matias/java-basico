
## Datas não têm formato
Uma data é apenas uma ideia, ou seja, ela representa um ponto específico no calendário. Assim, por exemplo, a data de "26 de março de 2019", pode ser representada seguinte forma:


- 26/03/2019 (um formato bem comum em muitos países, incluindo o Brasil)
- 3/26/2019 (formato americano, invertendo o dia e mês)
- 2019-03-26 (o formato ISO 8601)
- 26 de Março de 2019 (em bom português)
- March 26th, 2019 (em inglês)
- 2019年3月26日 (em japonês)



Então, uma data do tipo "DD/MM/YYYY" pode não ter uma representação muito precisa dependendo do contexto que ela estiver. 
Provavelmente você quer dizer que tem uma String neste formato? E que só vai trabalhar com o dia, mês e ano?

Assumindo as duas premissas acima (DD/MM/YYYY é o formato da String e você só precisa trabalhar com o dia, mês e ano), existem algumas soluções, que dependem da versão do Java que você está usando.
~~~Java
Date dataTeste = new Date();

Calendar cal = Calendar.getInstance(); 
cal.setTime(dataTeste ); 
cal.add(Calendar.DATE, 1);
dataTeste = cal.getTime();

~~~
