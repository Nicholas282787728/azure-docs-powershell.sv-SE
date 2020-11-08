---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 60d46a3d61f0799618107e9bc0727a3ff31fc337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922150"
---
# <span data-ttu-id="38d4f-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38d4f-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="38d4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="38d4f-103">Skapar ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="38d4f-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="38d4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38d4f-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38d4f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="38d4f-106">Cmdleten **New-AzApplicationGatewaySslCertificate** skapar ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="38d4f-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="38d4f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38d4f-107">EXAMPLES</span></span>

### <span data-ttu-id="38d4f-108">Exempel 1: skapa ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="38d4f-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="38d4f-109">Det här kommandot skapar ett SSL-certifikat med namnet Cert01 för standard program-gateway och lagrar resultatet i variabeln som heter $Cert.</span><span class="sxs-lookup"><span data-stu-id="38d4f-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="38d4f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38d4f-110">PARAMETERS</span></span>

### <span data-ttu-id="38d4f-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="38d4f-111">-CertificateFile</span></span>
<span data-ttu-id="38d4f-112">Anger sökvägen till. pfx-filen för SSL-certifikatet som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="38d4f-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d4f-113">-DefaultProfile</span></span>
<span data-ttu-id="38d4f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38d4f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d4f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="38d4f-115">-Name</span></span>
<span data-ttu-id="38d4f-116">Anger namnet på det SSL-certifikat som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="38d4f-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d4f-117">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="38d4f-117">-Password</span></span>
<span data-ttu-id="38d4f-118">Anger lösen ordet för SSL som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38d4f-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d4f-119">CommonParameters</span></span>
<span data-ttu-id="38d4f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d4f-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d4f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d4f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38d4f-122">INPUTS</span></span>

### <span data-ttu-id="38d4f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="38d4f-123">System.String</span></span>

## <span data-ttu-id="38d4f-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38d4f-124">OUTPUTS</span></span>

### <span data-ttu-id="38d4f-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38d4f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="38d4f-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38d4f-126">NOTES</span></span>

## <span data-ttu-id="38d4f-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38d4f-127">RELATED LINKS</span></span>

[<span data-ttu-id="38d4f-128">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38d4f-128">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="38d4f-129">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38d4f-129">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="38d4f-130">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38d4f-130">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="38d4f-131">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="38d4f-131">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)

