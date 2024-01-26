## Table 

Here is the table and right below it is the code to it






```shell
<div>
    <center>
        <br>
        <h2> Table - Users </h2>
        <br>

        <a href="{{ route('#') }}" class="btn btn-primary">Create User</a>
        <a href="{{route('#')}}" class="btn btn-primary">Create Profile</a>
    </center>

    <br><br>

    <div class="table">

        <table class="table table-bordered table-striped table-hover" name="table" id="id-tabela">
            <!-- Aqui vai ID da tabela -->
            <thead class="table-dark">
                <th scope='col'>Login</th>
                <th scope='col'>Name</th>
                <th scope='col'>Profile</th>
                <th scope='col'>Status</th>
                <th scope='col'>Action</th>

            </thead>
            <tbody>

                <tr>
                    <td>CAIORODRIG</td>
                    <td>Caio da Silveira Rodrigues</td>
                    <td>Master</td>
                    <td>Ativo</td>
                    <td>
                        <a href="#" class="btn btn-success">Edit</a>
                        <a href="" class="btn btn-success">Reset</a>
                    </td>

                </tr>

            </tbody>
        </table>
    </div>

</div>


<!-- Adicionando Jquery -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script src="js/jquery.dataTables.min.js"></script>



<script>
    $(document).ready(function() {
        $('#id-tabela').DataTable({
            "language": {
                "lengthMenu": "Mostrando _MENU_ Registros por página",
                "zeroRecords": "Nenhum dado foi encontrado.",
                "info": "Mostrando página _PAGE_ de _PAGES_",
                "infoEmpty": "Nenhum registro encontrado - vazio",
                "infoFiltered": "(Filtrados de  _MAX_ registros no total)"
            }
        }); //id da tabela
    });

    $(document).ready(function() {
        $('#id-tabela2').DataTable({
            "language": {
                "lengthMenu": "Mostrando _MENU_ Registros por página",
                "zeroRecords": "Nenhum dado foi encontrado.",
                "info": "Mostrando página _PAGE_ de _PAGES_",
                "infoEmpty": "Nenhum registro encontrado - vazio",
                "infoFiltered": "(Filtrados de  _MAX_ registros no total)"
            }
        }); //id da tabela
    });
</script>




<script type="text/javascript">
    document.getElementById("downloadexcel").addEventListener('click', function() {
        var table2excel = new Table2Excel();
        table2excel.export(document.querySelectorAll("#id-tabela"));
    });
</script>
<script type="text/javascript" src="assets/script.js"></script>



</div>
```
