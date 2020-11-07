---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: ed5a2d3d004dfe1480d14e598b009cf6e49d2c1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917989"
---
# <span data-ttu-id="f84b2-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f84b2-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="f84b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f84b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f84b2-103">Tar bort ett befintligt rot certifikat för en VPN-klient.</span><span class="sxs-lookup"><span data-stu-id="f84b2-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="f84b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f84b2-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f84b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f84b2-105">DESCRIPTION</span></span>
<span data-ttu-id="f84b2-106">Cmdleten **Remove-AzVpnClientRootCertificate** tar bort det angivna rot certifikatet från en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="f84b2-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="f84b2-107">Rot certifikat är 509 certifikat som identifierar rot certifikat utfärdaren: alla andra certifikat som används på gatewayen har rot certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f84b2-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="f84b2-108">Om du tar bort en rot certifikat dator som använder certifikatet för verifiering kommer inte längre att kunna ansluta till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f84b2-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="f84b2-109">När du använder **Remove-AzVpnClientRootCertificate** måste du ange både certifikat namnet och en text representation av certifikat data.</span><span class="sxs-lookup"><span data-stu-id="f84b2-109">When you use **Remove-AzVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="f84b2-110">Mer information om hur du visar text i ett certifikat finns i beskrivningen av *PublicCertData* -parametern.</span><span class="sxs-lookup"><span data-stu-id="f84b2-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="f84b2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f84b2-111">EXAMPLES</span></span>

### <span data-ttu-id="f84b2-112">Exempel 1: ta bort ett klient rot certifikat från en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="f84b2-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="f84b2-113">I det här exemplet tas klient rot certifikatet bort med namnet ContosoRootCertificate från den virtuella Nätverksgatewayen ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="f84b2-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="f84b2-114">I det första kommandot används cmdleten **Get-Content** för att få en tidigare exporterad text från certifikatet; den här text presentationen lagras i en variabel som heter $Text.</span><span class="sxs-lookup"><span data-stu-id="f84b2-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="f84b2-115">Det andra kommandot använder sedan en for-slinga för att extrahera all text i $Text förutom den första raden och den sista raden.</span><span class="sxs-lookup"><span data-stu-id="f84b2-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="f84b2-116">Den extraherade texten lagras i en variabel som heter $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="f84b2-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="f84b2-117">Det tredje kommandot använder informationen som lagras i $CertificateText variabel tillsammans med cmdleten **Remove-AzVpnClientRootCertificate** för att ta bort certifikatet från gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f84b2-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="f84b2-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f84b2-118">PARAMETERS</span></span>

### <span data-ttu-id="f84b2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84b2-119">-DefaultProfile</span></span>
<span data-ttu-id="f84b2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f84b2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f84b2-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="f84b2-121">-PublicCertData</span></span>
<span data-ttu-id="f84b2-122">Anger text åter givningen för det rot certifikat som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f84b2-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="f84b2-123">För att få text presentationen exporterar du certifikatet i CER-format (med base64-kodning) och öppnar sedan den resulterande filen i en text redigerare.</span><span class="sxs-lookup"><span data-stu-id="f84b2-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="f84b2-124">Utdata ser ut ungefär så här (Observera att den faktiska utmatningen innehåller många fler text rader än det förkortade exemplet visas här):-----starta certifikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----avsluta certifikatet-----PublicCertData är upptaget av alla linjer mellan den första raden (-----BEGIN CERTIFICATe-----) och den sista raden (-----slut certifikat-----) i filen.</span><span class="sxs-lookup"><span data-stu-id="f84b2-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="f84b2-125">Du kan hämta PublicCertData med hjälp av Windows PowerShell-kommandon som den här: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = för ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="f84b2-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="f84b2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84b2-126">-ResourceGroupName</span></span>
<span data-ttu-id="f84b2-127">Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="f84b2-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="f84b2-128">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="f84b2-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="f84b2-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f84b2-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f84b2-130">Anger namnet på den virtuella nätverksgateway som certifikatet tas bort från.</span><span class="sxs-lookup"><span data-stu-id="f84b2-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="f84b2-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="f84b2-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="f84b2-132">Anger namnet på klient rot certifikatet som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="f84b2-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f84b2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84b2-133">CommonParameters</span></span>
<span data-ttu-id="f84b2-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84b2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84b2-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f84b2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84b2-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f84b2-136">INPUTS</span></span>

### <span data-ttu-id="f84b2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f84b2-137">System.String</span></span>

## <span data-ttu-id="f84b2-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f84b2-138">OUTPUTS</span></span>

### <span data-ttu-id="f84b2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f84b2-139">System.Boolean</span></span>

## <span data-ttu-id="f84b2-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f84b2-140">NOTES</span></span>

## <span data-ttu-id="f84b2-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f84b2-141">RELATED LINKS</span></span>

[<span data-ttu-id="f84b2-142">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f84b2-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="f84b2-143">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f84b2-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="f84b2-144">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f84b2-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


