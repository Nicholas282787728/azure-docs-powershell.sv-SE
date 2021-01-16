---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410560"
---
# <span data-ttu-id="ae569-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae569-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="ae569-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae569-102">SYNOPSIS</span></span>
<span data-ttu-id="ae569-103">Lägger till en VPN-klient rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="ae569-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="ae569-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae569-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae569-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae569-105">DESCRIPTION</span></span>
<span data-ttu-id="ae569-106">Cmdleten **Add-AzVpnClientRootCertificate** lägger till ett rot certifikat till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="ae569-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="ae569-107">Rot certifikat är 509 certifikat som identifierar din rot certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="ae569-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="ae569-108">Efter design är rot certifikatet som används på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ae569-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="ae569-109">Denna cmdlet tilldelar ett befintligt certifikat som ett Gateway-rotcertifikat.</span><span class="sxs-lookup"><span data-stu-id="ae569-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="ae569-110">Om du inte har något 509-certifikat tillgängligt kan du skapa ett via din offentliga infrastruktur eller använda en certifikat generator, till exempel makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="ae569-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="ae569-111">Om du vill lägga till ett rot certifikat måste du ange certifikat namnet och tillhandahålla en representation av certifikatet (se *PublicCertData* -parametern för mer information).</span><span class="sxs-lookup"><span data-stu-id="ae569-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="ae569-112">Med Azure kan du tilldela mer än ett rot certifikat till en gateway.</span><span class="sxs-lookup"><span data-stu-id="ae569-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="ae569-113">Flera rot certifikat distribueras ofta av organisationer som innehåller användare från mer än ett företag.</span><span class="sxs-lookup"><span data-stu-id="ae569-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="ae569-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae569-114">EXAMPLES</span></span>

### <span data-ttu-id="ae569-115">Exempel 1: lägga till ett klient rot certifikat till en virtuell gateway</span><span class="sxs-lookup"><span data-stu-id="ae569-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="ae569-116">Det här exemplet lägger till ett klient rot certifikat till en virtuell gateway med namnet ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="ae569-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="ae569-117">I det första kommandot används cmdleten **Get-Content** för att få en tidigare exporterad text av rot certifikatet och lagrar text data som variabeln $text.</span><span class="sxs-lookup"><span data-stu-id="ae569-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="ae569-118">Det andra kommandot använder sedan en for-slinga för att extrahera all text förutom den första raden och den sista raden.</span><span class="sxs-lookup"><span data-stu-id="ae569-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="ae569-119">Den extraherade texten lagras i en variabel som heter $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="ae569-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="ae569-120">Det tredje kommandot använder sedan den text som lagras i $CertificateText med cmdleten **Add-AzVpnClientRootCertificate** för att lägga till rot certifikatet till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ae569-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="ae569-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae569-121">PARAMETERS</span></span>

### <span data-ttu-id="ae569-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae569-122">-DefaultProfile</span></span>
<span data-ttu-id="ae569-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae569-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae569-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="ae569-124">-PublicCertData</span></span>
<span data-ttu-id="ae569-125">Anger text representationen för det rot certifikat som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="ae569-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="ae569-126">För att få text presentationen exporterar du certifikatet i CER-format (med base64-kodning) och öppnar sedan den resulterande filen i en text redigerare.</span><span class="sxs-lookup"><span data-stu-id="ae569-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="ae569-127">När du gör det ser du utdata som liknar följande (Observera att den faktiska utmatningen innehåller många fler text rader än det förkortade provet som visas här):-----starta certifikatet-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----avsluta certifikatet-----PublicCertData är upptaget av alla linjer mellan den första raden (-----BEGIN CERTIFICATe-----) på filen.</span><span class="sxs-lookup"><span data-stu-id="ae569-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="ae569-128">Du kan hämta dessa data genom att använda Windows PowerShell-kommandon som det här: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="ae569-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae569-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae569-129">-ResourceGroupName</span></span>
<span data-ttu-id="ae569-130">Anger namnet på resurs gruppen som rot certifikatet är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="ae569-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="ae569-131">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="ae569-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae569-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ae569-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ae569-133">Anger namnet på den virtuella nätverksgateway där certifikatet läggs till.</span><span class="sxs-lookup"><span data-stu-id="ae569-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae569-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="ae569-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="ae569-135">Anger namnet på klient rot certifikatet som läggs till av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae569-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae569-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae569-136">CommonParameters</span></span>
<span data-ttu-id="ae569-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae569-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae569-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae569-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae569-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae569-139">INPUTS</span></span>

### <span data-ttu-id="ae569-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ae569-140">System.String</span></span>

## <span data-ttu-id="ae569-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae569-141">OUTPUTS</span></span>

### <span data-ttu-id="ae569-142">Microsoft. Azure. commands. Networks. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae569-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="ae569-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae569-143">NOTES</span></span>

## <span data-ttu-id="ae569-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae569-144">RELATED LINKS</span></span>

[<span data-ttu-id="ae569-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae569-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="ae569-146">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae569-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="ae569-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae569-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


