---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cec5a6aa0b61889e7923ebce67d1247f99d215e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757496"
---
# <span data-ttu-id="7dbe7-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7dbe7-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="7dbe7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7dbe7-102">SYNOPSIS</span></span>
<span data-ttu-id="7dbe7-103">Anger mål tillstånd för ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="7dbe7-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dbe7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7dbe7-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dbe7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7dbe7-105">DESCRIPTION</span></span>
<span data-ttu-id="7dbe7-106">Cmdleten **set-AzureRmApplicationGatewaySslCertificate** anger mål tillståndet för ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="7dbe7-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="7dbe7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7dbe7-107">EXAMPLES</span></span>

### <span data-ttu-id="7dbe7-108">Exempel 1: Ange mål tillstånd för ett SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="7dbe7-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="7dbe7-109">Det här kommandot anger mål tillståndet för ett SSL-certifikat från den Programgateway som heter ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="7dbe7-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="7dbe7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7dbe7-110">PARAMETERS</span></span>

### <span data-ttu-id="7dbe7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7dbe7-111">-ApplicationGateway</span></span>
<span data-ttu-id="7dbe7-112">Anger den Programgateway som certifikatet för SSL (Secure Socket Layer) är associerat med.</span><span class="sxs-lookup"><span data-stu-id="7dbe7-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbe7-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7dbe7-113">-CertificateFile</span></span>
<span data-ttu-id="7dbe7-114">Anger sökvägen till SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="7dbe7-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="7dbe7-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7dbe7-115">-Name</span></span>
<span data-ttu-id="7dbe7-116">Anger namnet på SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="7dbe7-116">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="7dbe7-117">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="7dbe7-117">-Password</span></span>
<span data-ttu-id="7dbe7-118">Anger lösen ordet för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="7dbe7-118">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="7dbe7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dbe7-119">-DefaultProfile</span></span>
<span data-ttu-id="7dbe7-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7dbe7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dbe7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dbe7-121">CommonParameters</span></span>
<span data-ttu-id="7dbe7-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dbe7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dbe7-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dbe7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dbe7-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7dbe7-124">INPUTS</span></span>

### <span data-ttu-id="7dbe7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7dbe7-125">System.String</span></span>

## <span data-ttu-id="7dbe7-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7dbe7-126">OUTPUTS</span></span>

### <span data-ttu-id="7dbe7-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7dbe7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7dbe7-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7dbe7-128">NOTES</span></span>

## <span data-ttu-id="7dbe7-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7dbe7-129">RELATED LINKS</span></span>

[<span data-ttu-id="7dbe7-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7dbe7-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7dbe7-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7dbe7-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7dbe7-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7dbe7-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7dbe7-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7dbe7-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


