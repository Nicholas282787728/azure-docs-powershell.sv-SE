---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271477"
---
# <span data-ttu-id="0ebf4-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0ebf4-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="0ebf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ebf4-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebf4-103">Skapar ett nytt rot certifikat för en VPN-klient.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="0ebf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ebf4-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ebf4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ebf4-105">DESCRIPTION</span></span>
<span data-ttu-id="0ebf4-106">Cmdleten **New-AzVpnClientRootCertificate** skapar ett nytt VPN-rotcertifikat för användning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="0ebf4-107">Rot certifikat är 509 certifikat som identifierar rot certifikat utfärdaren: alla andra certifikat som används på gatewayen har rot certifikatet.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="0ebf4-108">Denna cmdlet skapar ett fristående certifikat som inte är kopplat till en virtuell gateway.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="0ebf4-109">I stället används certifikatet som skapas av **New-AzVpnClientRootCertificate** tillsammans med New-AzVirtualNetworkGateway cmdlet när du skapar en ny Gateway.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="0ebf4-110">Anta till exempel att du skapar ett nytt certifikat och lagrar det i en variabel som heter $Certificate.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="0ebf4-111">Du kan sedan använda detta certifikat objekt när du skapar en ny virtuell gateway.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="0ebf4-112">Till exempel: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="0ebf4-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="0ebf4-113">Mer information finns i dokumentationen för New-AzVirtualNetworkGateway-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="0ebf4-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ebf4-114">EXAMPLES</span></span>

### <span data-ttu-id="0ebf4-115">Exempel 1: skapa ett klient rot certifikat</span><span class="sxs-lookup"><span data-stu-id="0ebf4-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="0ebf4-116">I det här exemplet skapas ett klient rot certifikat och ett certifikat objekt sparas i en variabel som heter $Certificate.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="0ebf4-117">Denna variabel kan sedan användas av **New-AzVirtualNetworkGateway-** cmdleten för att lägga till ett rot certifikat till en ny virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="0ebf4-118">I det första kommandot används cmdleten **Get-Content** för att få en tidigare exporterad text representation av rot certifikatet. att text data lagras i en variabel som heter $Text.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="0ebf4-119">Det andra kommandot använder sedan en for-slinga för att extrahera all text förutom den första raden och den sista raden, och sedan spara den extraherade texten i en variabel som heter $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="0ebf4-120">I det tredje kommandot används cmdleten **New-AzVpnClientRootCertificate** för att skapa certifikatet, vilket sparar det skapade objektet i en variabel som heter $Certificate.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="0ebf4-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ebf4-121">PARAMETERS</span></span>

### <span data-ttu-id="0ebf4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebf4-122">-DefaultProfile</span></span>
<span data-ttu-id="0ebf4-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ebf4-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ebf4-124">-Name</span></span>
<span data-ttu-id="0ebf4-125">Anger ett namn för det nya klient rot certifikatet.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-125">Specifies a name for the new client root certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebf4-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="0ebf4-126">-PublicCertData</span></span>
<span data-ttu-id="0ebf4-127">Anger en text representation av rot certifikatet som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="0ebf4-128">För att få text presentationen exporterar du certifikatet i CER-format (med base64-kodning) och öppnar sedan den resulterande filen i en text redigerare.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="0ebf4-129">Utdata ser ut ungefär så här (Observera att den faktiska utmatningen innehåller många fler text rader än det förkortade provet som visas här):-----starta certifikatet-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----avsluta certifikat-----PublicCertData är upptaget av alla linjer mellan den första raden (-----BEGIN CERTIFICATe-----) och den sista raden (-----slut certifikat-----) i filen.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="0ebf4-130">Du kan hämta PublicCertData med hjälp av Windows PowerShell-kommandon som liknar detta: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = för ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="0ebf4-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="0ebf4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebf4-131">CommonParameters</span></span>
<span data-ttu-id="0ebf4-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebf4-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebf4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebf4-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ebf4-134">INPUTS</span></span>

### <span data-ttu-id="0ebf4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0ebf4-135">System.String</span></span>

## <span data-ttu-id="0ebf4-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ebf4-136">OUTPUTS</span></span>

### <span data-ttu-id="0ebf4-137">Microsoft. Azure. commands. Networks. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0ebf4-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="0ebf4-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ebf4-138">NOTES</span></span>

## <span data-ttu-id="0ebf4-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ebf4-139">RELATED LINKS</span></span>

[<span data-ttu-id="0ebf4-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0ebf4-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="0ebf4-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0ebf4-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="0ebf4-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0ebf4-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


