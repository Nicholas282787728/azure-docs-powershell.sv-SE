---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1af7ef3b60fa296a5fb8190675393a0726d0502b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574888"
---
# <span data-ttu-id="9029a-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9029a-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9029a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9029a-102">SYNOPSIS</span></span>
<span data-ttu-id="9029a-103">Anger mål tillstånd för ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="9029a-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9029a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9029a-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9029a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9029a-105">DESCRIPTION</span></span>
<span data-ttu-id="9029a-106">Cmdleten **set-AzureRmApplicationGatewaySslCertificate** anger mål tillståndet för ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="9029a-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="9029a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9029a-107">EXAMPLES</span></span>

### <span data-ttu-id="9029a-108">Exempel 1: Ange mål tillstånd för ett SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="9029a-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="9029a-109">Det här kommandot anger mål tillståndet för ett SSL-certifikat från den Programgateway som heter ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="9029a-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="9029a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9029a-110">PARAMETERS</span></span>

### <span data-ttu-id="9029a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9029a-111">-ApplicationGateway</span></span>
<span data-ttu-id="9029a-112">Anger den Programgateway som certifikatet för SSL (Secure Socket Layer) är associerat med.</span><span class="sxs-lookup"><span data-stu-id="9029a-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="9029a-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9029a-113">-CertificateFile</span></span>
<span data-ttu-id="9029a-114">Anger sökvägen till SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9029a-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="9029a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9029a-115">-DefaultProfile</span></span>
<span data-ttu-id="9029a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9029a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9029a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="9029a-117">-Name</span></span>
<span data-ttu-id="9029a-118">Anger namnet på SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9029a-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="9029a-119">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="9029a-119">-Password</span></span>
<span data-ttu-id="9029a-120">Anger lösen ordet för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9029a-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="9029a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9029a-121">CommonParameters</span></span>
<span data-ttu-id="9029a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9029a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9029a-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9029a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9029a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9029a-124">INPUTS</span></span>

### <span data-ttu-id="9029a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9029a-125">System.String</span></span>

## <span data-ttu-id="9029a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9029a-126">OUTPUTS</span></span>

### <span data-ttu-id="9029a-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9029a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9029a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9029a-128">NOTES</span></span>

## <span data-ttu-id="9029a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9029a-129">RELATED LINKS</span></span>

[<span data-ttu-id="9029a-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9029a-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9029a-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9029a-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9029a-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9029a-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9029a-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9029a-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


