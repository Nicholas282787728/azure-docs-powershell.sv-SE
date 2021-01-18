---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 1763dfab6815efd625ff43ee248664a3f7b36cb9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525806"
---
# <span data-ttu-id="e019f-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e019f-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="e019f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e019f-102">SYNOPSIS</span></span>
<span data-ttu-id="e019f-103">Uppdaterar SSL-profilen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e019f-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="e019f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e019f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e019f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e019f-105">DESCRIPTION</span></span>
<span data-ttu-id="e019f-106">Cmdleten **set-AzApplicationGatewaySslProfile** uppdaterar SSL-profilen för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e019f-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="e019f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e019f-107">EXAMPLES</span></span>

### <span data-ttu-id="e019f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e019f-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="e019f-109">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="e019f-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="e019f-110">Det andra kommandot uppdaterar SSL-profilen för programgatewayen i $AppGw variabel för att uppdatera konfigurationen för klientautentisering till det nya värdet som lagras i $newclientconfig.</span><span class="sxs-lookup"><span data-stu-id="e019f-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="e019f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e019f-111">PARAMETERS</span></span>

### <span data-ttu-id="e019f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e019f-112">-ApplicationGateway</span></span>
<span data-ttu-id="e019f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e019f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e019f-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="e019f-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="e019f-115">Konfigurations inställningar för klientautentisering</span><span class="sxs-lookup"><span data-stu-id="e019f-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e019f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e019f-116">-DefaultProfile</span></span>
<span data-ttu-id="e019f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e019f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e019f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e019f-118">-Name</span></span>
<span data-ttu-id="e019f-119">Namnet på SSL-profilen</span><span class="sxs-lookup"><span data-stu-id="e019f-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="e019f-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="e019f-120">-SslPolicy</span></span>
<span data-ttu-id="e019f-121">SSL-princip</span><span class="sxs-lookup"><span data-stu-id="e019f-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e019f-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="e019f-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="e019f-123">Den betrodda klient certifikat utfärdarens certifikat kedjor</span><span class="sxs-lookup"><span data-stu-id="e019f-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e019f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e019f-124">CommonParameters</span></span>
<span data-ttu-id="e019f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e019f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e019f-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e019f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e019f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e019f-127">INPUTS</span></span>

### <span data-ttu-id="e019f-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e019f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e019f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e019f-129">OUTPUTS</span></span>

### <span data-ttu-id="e019f-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e019f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e019f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e019f-131">NOTES</span></span>

## <span data-ttu-id="e019f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e019f-132">RELATED LINKS</span></span>

[<span data-ttu-id="e019f-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e019f-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="e019f-134">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e019f-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="e019f-135">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e019f-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="e019f-136">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e019f-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)