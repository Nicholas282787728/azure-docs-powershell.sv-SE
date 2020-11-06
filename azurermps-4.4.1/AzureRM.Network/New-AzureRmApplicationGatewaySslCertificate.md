---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: ad318c776662ebaeab3192ca584aa2aad7f2e20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576706"
---
# <span data-ttu-id="8eaf1-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8eaf1-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8eaf1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8eaf1-102">SYNOPSIS</span></span>
<span data-ttu-id="8eaf1-103">Skapar ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8eaf1-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eaf1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8eaf1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eaf1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8eaf1-105">DESCRIPTION</span></span>
<span data-ttu-id="8eaf1-106">Cmdleten **New-AzureRmApplicationGatewaySslCertificate** skapar ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8eaf1-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8eaf1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8eaf1-107">EXAMPLES</span></span>

### <span data-ttu-id="8eaf1-108">Exempel 1: skapa ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8eaf1-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\>$Cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="8eaf1-109">Det här kommandot skapar ett SSL-certifikat med namnet Cert01 för standard program-gateway och lagrar resultatet i variabeln som heter $Cert.</span><span class="sxs-lookup"><span data-stu-id="8eaf1-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="8eaf1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8eaf1-110">PARAMETERS</span></span>

### <span data-ttu-id="8eaf1-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8eaf1-111">-CertificateFile</span></span>
<span data-ttu-id="8eaf1-112">Anger sökvägen till. pfx-filen för SSL-certifikatet som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="8eaf1-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8eaf1-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8eaf1-113">-Name</span></span>
<span data-ttu-id="8eaf1-114">Anger namnet på det SSL-certifikat som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="8eaf1-114">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8eaf1-115">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="8eaf1-115">-Password</span></span>
<span data-ttu-id="8eaf1-116">Anger lösen ordet för SSL som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eaf1-116">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8eaf1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eaf1-117">-DefaultProfile</span></span>
<span data-ttu-id="8eaf1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8eaf1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eaf1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eaf1-119">CommonParameters</span></span>
<span data-ttu-id="8eaf1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eaf1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eaf1-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eaf1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eaf1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8eaf1-122">INPUTS</span></span>

### <span data-ttu-id="8eaf1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8eaf1-123">System.String</span></span>

## <span data-ttu-id="8eaf1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8eaf1-124">OUTPUTS</span></span>

### <span data-ttu-id="8eaf1-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8eaf1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8eaf1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8eaf1-126">NOTES</span></span>

## <span data-ttu-id="8eaf1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8eaf1-127">RELATED LINKS</span></span>

[<span data-ttu-id="8eaf1-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8eaf1-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8eaf1-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8eaf1-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8eaf1-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8eaf1-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8eaf1-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8eaf1-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


