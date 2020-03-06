# Atividades para serem desenvolvidas utilizando JavaIO

1 - Com base no repositorio apresentado em sala, gravar em um arquivo .csv os dados de um Objeto pessoa, que além do nome e email contenha a data de nascimento da Pessoa.
    Nos metodos set e get da classe criar as validações para e-mail e data de nascimento.
    -> No metodo setEmail só permitir que seja inserido um e-mail valido no atributo
    -> No metodo getDatNascimento retornar a data de nascimento + a idade da Pessoa
    -> No metodo setDatNascimento só permitir que a pessoa tenha mais de 18 anos. * A data deve ser passada para a classe no seguinte formato ("dd/mm/yyyy") e salva no arquivo ("yyyy-mm-dd").
    
    ```
    //    Pattern	Example
    //    dd-MM-yy	31-01-12
    //    dd-MM-yyyy	31-01-2012
    //    MM-dd-yyyy	01-31-2012
    //    yyyy-MM-dd	2012-01-31
    //    yyyy-MM-dd HH:mm:ss	2012-01-31 23:59:59
    //    yyyy-MM-dd HH:mm:ss.SSS	2012-01-31 23:59:59.999
    //    yyyy-MM-dd HH:mm:ss.SSSZ	2012-01-31 23:59:59.999+0100
    //    EEEEE MMMMM yyyy HH:mm:ss.SSSZ	Saturday November 2012 10:45:42.720+0100
        String nascimento = "13/02/1997";
        String nascimento = "1997-13-02";
        nascimento = nascimento.replaceAll("/", "-");
        String pattern = "dd-MM-yyyy";
        String pattern = "yyyy-dd-MM";
        DateFormat formatter = new SimpleDateFormat(pattern);
        Date data = formatter.parse(nascimento);
        System.out.println(formatter.format(data));
        System.out.println(data.toString());
    ```
