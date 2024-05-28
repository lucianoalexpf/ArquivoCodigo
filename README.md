# ArquivoCodigo
Local para armazenar códigos

Obj DataGridView

####################
> Como adicionar uma linha no DataGridView
Grid.Rows.Add();

> Como deixar uma DataGridView com apenas a linha do cabeçalho
Grid.

> Como deixar uma linha da DataGridView selecionada via código
Grid.SelectionMode = DataGridViewSelectionMode.FullRowSelect;

> Não deixar selecionar mais que uma linha no DataGridView
Grid.MultiSelect = false;

> Deixar a DataGridView ocupat todo o espaçamento do obejto que ele está inserido
Grid.Dock = DockStyle.Fill;

> Pegar o índice da linha selecionada
Grid.SelectedRows[0].Index;

> Deletar uma linha da DataGridView
Grid.Rows.RemoveAt(
                Grid.SelectedRows[0].Index
);

> Configurar uma DataGridView
private void ConfigGrid()
    {
        Grid.ColumnCount = 5;

        Grid.ColumnHeadersDefaultCellStyle.BackColor = Color.Navy;
        Grid.ColumnHeadersDefaultCellStyle.ForeColor = Color.White;
        Grid.ColumnHeadersDefaultCellStyle.Font =
            new Font(Grid.Font, FontStyle.Bold);

        Grid.Name = "Grid";
        Grid.Location = new Point(8, 8);
        Grid.Size = new Size(500, 250);
        Grid.AutoSizeRowsMode =
            Grid.DisplayedCellsExceptHeaders;
        Grid.ColumnHeadersBorderStyle =
            Grid.Single;
        Grid.CellBorderStyle = DataGridViewCellBorderStyle.Single;
        Grid.GridColor = Color.Black;
        Grid.RowHeadersVisible = false;

        Grid.Columns[0].Name = "Release Date";
        Grid.Columns[1].Name = "Track";
        Grid.Columns[2].Name = "Title";
        Grid.Columns[3].Name = "Artist";
        Grid.Columns[4].Name = "Album";
        Grid.Columns[4].DefaultCellStyle.Font =
            new Font(Grid.DefaultCellStyle.Font, FontStyle.Italic);

        Grid.SelectionMode =
            DataGridViewSelectionMode.FullRowSelect;
        Grid.MultiSelect = false;
        Grid.Dock = DockStyle.Fill;

        Grid.CellFormatting += new
            DataGridViewCellFormattingEventHandler(
            Grid_CellFormatting);
    }
