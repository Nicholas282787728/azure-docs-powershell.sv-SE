---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273225"
---
# <span data-ttu-id="ca759-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca759-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="ca759-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca759-102">SYNOPSIS</span></span>
<span data-ttu-id="ca759-103">Hämtar den privata länk konfigurationen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ca759-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="ca759-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca759-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca759-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca759-105">DESCRIPTION</span></span>
<span data-ttu-id="ca759-106">Cmdleten **Get-AzApplicationGatewayPrivateLinkConfiguration** hämtar den privata länk konfigurationen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ca759-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="ca759-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca759-107">EXAMPLES</span></span>

### <span data-ttu-id="ca759-108">Exempel 1: Hämta en angiven konfiguration för privat länk</span><span class="sxs-lookup"><span data-stu-id="ca759-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="ca759-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 från resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="ca759-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ca759-110">Med det andra kommandot hämtas den privata länk konfigurationen med namnet privateLinkConfig01 från $AppGw och lagras i $PrivateLinkConfiguration-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ca759-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="ca759-111">Exempel 2: Hämta en lista med konfiguration för privat länk</span><span class="sxs-lookup"><span data-stu-id="ca759-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="ca759-112">Det första kommandot får en Programgateway som heter ApplicationGateway01 från resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="ca759-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ca759-113">Med det andra kommandot hämtas alla konfigurationer för privata länkar från $AppGw och lagras i $PrivateLinkConfigurations-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ca759-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="ca759-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca759-114">PARAMETERS</span></span>

### <span data-ttu-id="ca759-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca759-115">-ApplicationGateway</span></span>
<span data-ttu-id="ca759-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca759-116">The applicationGateway</span></span>

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

### <span data-ttu-id="ca759-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca759-117">-DefaultProfile</span></span>
<span data-ttu-id="ca759-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca759-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca759-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca759-119">-Name</span></span>
<span data-ttu-id="ca759-120">Namnet på privateLink-konfigurationen för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ca759-120">The name of the application gateway privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca759-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca759-121">CommonParameters</span></span>
<span data-ttu-id="ca759-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca759-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca759-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca759-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca759-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca759-124">INPUTS</span></span>

### <span data-ttu-id="ca759-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca759-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ca759-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca759-126">OUTPUTS</span></span>

### <span data-ttu-id="ca759-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca759-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="ca759-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca759-128">NOTES</span></span>

## <span data-ttu-id="ca759-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca759-129">RELATED LINKS</span></span>

[<span data-ttu-id="ca759-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca759-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ca759-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca759-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ca759-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca759-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ca759-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca759-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)