---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: bb295ba9f1b7c446e8f8fd6e80d8445774bf8852
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929666"
---
# <span data-ttu-id="5a086-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5a086-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5a086-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a086-102">SYNOPSIS</span></span>
<span data-ttu-id="5a086-103">Anger mål tillstånd för ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="5a086-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a086-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a086-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a086-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a086-105">DESCRIPTION</span></span>
<span data-ttu-id="5a086-106">Cmdleten **set-AzureRmApplicationGatewaySslCertificate** anger mål tillståndet för ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="5a086-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="5a086-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a086-107">EXAMPLES</span></span>

### <span data-ttu-id="5a086-108">Exempel 1: Ange mål tillstånd för ett SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="5a086-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="5a086-109">Det här kommandot anger mål tillståndet för ett SSL-certifikat från den Programgateway som heter ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="5a086-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="5a086-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a086-110">PARAMETERS</span></span>

### <span data-ttu-id="5a086-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a086-111">-ApplicationGateway</span></span>
<span data-ttu-id="5a086-112">Anger den Programgateway som certifikatet för SSL (Secure Socket Layer) är associerat med.</span><span class="sxs-lookup"><span data-stu-id="5a086-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="5a086-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5a086-113">-CertificateFile</span></span>
<span data-ttu-id="5a086-114">Anger sökvägen till SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="5a086-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="5a086-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a086-115">-DefaultProfile</span></span>
<span data-ttu-id="5a086-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a086-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a086-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a086-117">-Name</span></span>
<span data-ttu-id="5a086-118">Anger namnet på SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="5a086-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="5a086-119">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="5a086-119">-Password</span></span>
<span data-ttu-id="5a086-120">Anger lösen ordet för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="5a086-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="5a086-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a086-121">CommonParameters</span></span>
<span data-ttu-id="5a086-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a086-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a086-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a086-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a086-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a086-124">INPUTS</span></span>

### <span data-ttu-id="5a086-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5a086-125">System.String</span></span>

## <span data-ttu-id="5a086-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a086-126">OUTPUTS</span></span>

### <span data-ttu-id="5a086-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a086-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5a086-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a086-128">NOTES</span></span>

## <span data-ttu-id="5a086-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a086-129">RELATED LINKS</span></span>

[<span data-ttu-id="5a086-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5a086-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5a086-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5a086-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5a086-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5a086-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5a086-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5a086-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


