---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: eeab1f5699af5de737bc1e0390c35d387acfdd98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929321"
---
# <span data-ttu-id="e9f4a-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9f4a-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e9f4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f4a-103">Tar bort ett SSL-certifikat från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e9f4a-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9f4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9f4a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9f4a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9f4a-105">DESCRIPTION</span></span>
<span data-ttu-id="e9f4a-106">Cmdleten **Remove-AzureRmApplicationGatewaySslCertificate** tar bort ett SSL-certifikat från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e9f4a-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="e9f4a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9f4a-107">EXAMPLES</span></span>

### <span data-ttu-id="e9f4a-108">Exempel 1: ta bort ett SSL-certifikat från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="e9f4a-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="e9f4a-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e9f4a-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="e9f4a-110">Det andra kommandot tar bort SSL-certifikatet som heter Cert02 från Application Gateway som lagras i $AppGW variabel.</span><span class="sxs-lookup"><span data-stu-id="e9f4a-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="e9f4a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9f4a-111">PARAMETERS</span></span>

### <span data-ttu-id="e9f4a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9f4a-112">-ApplicationGateway</span></span>
<span data-ttu-id="e9f4a-113">Anger den Programgateway som den här cmdleten tar bort ett SSL-certifikat från.</span><span class="sxs-lookup"><span data-stu-id="e9f4a-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f4a-114">-DefaultProfile</span></span>
<span data-ttu-id="e9f4a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9f4a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9f4a-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9f4a-116">-Name</span></span>
<span data-ttu-id="e9f4a-117">Anger namnet på ett SSL-certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e9f4a-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e9f4a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f4a-118">CommonParameters</span></span>
<span data-ttu-id="e9f4a-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f4a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f4a-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f4a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f4a-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9f4a-121">INPUTS</span></span>

### <span data-ttu-id="e9f4a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e9f4a-122">System.String</span></span>

## <span data-ttu-id="e9f4a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9f4a-123">OUTPUTS</span></span>

### <span data-ttu-id="e9f4a-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9f4a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9f4a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9f4a-125">NOTES</span></span>

## <span data-ttu-id="e9f4a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9f4a-126">RELATED LINKS</span></span>

[<span data-ttu-id="e9f4a-127">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9f4a-127">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e9f4a-128">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9f4a-128">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e9f4a-129">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9f4a-129">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e9f4a-130">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9f4a-130">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


