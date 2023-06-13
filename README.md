# ObtenerEdad
Program that obtains and shows the age through a visual interface
Public Class FormPrincipal

    Private Sub BtnObtenerEdad_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles BtnObtenerEdad.Click
        Dim strResultado As String
        Dim intEdad As Integer

        strResultado = InputBox("Por Favor, escriba su edad.", "Escriba su edad")

        If strResultado = "" Then
            MessageBox.Show("Ha hecho clic sobre el boton Cancelar.")
        ElseIf IsNumeric(strResultado) Then
            'El usuario ha introducido un numero.
            'Almacenarlo en la variable intEdad como numero.
            intEdad = CInt(strResultado)
            MessageBox.Show("Ha escrito el valor " & intEdad & ".")
        Else
            MessageBox.Show("No ha introducido un numero.")

        End If
    End Sub
End Class
