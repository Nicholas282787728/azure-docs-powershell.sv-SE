---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272899"
---
# <span data-ttu-id="d8327-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8327-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="d8327-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8327-102">SYNOPSIS</span></span>
<span data-ttu-id="d8327-103">Skapar en privat länk konfiguration för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="d8327-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="d8327-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8327-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8327-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8327-105">DESCRIPTION</span></span>
<span data-ttu-id="d8327-106">Cmdleten **New-AzApplicationGatewayPrivateLinkConfiguration** skapar en PrivateLink-konfiguration för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d8327-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="d8327-107">Konfigurationen för den privata länken måste kopplas till en IP-konfiguration för klient delen för att aktivera funktionen för privat länk.</span><span class="sxs-lookup"><span data-stu-id="d8327-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="d8327-108">En privat länk konfiguration kan atmost associeras med bara en klient dels-IP-konfiguration på Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d8327-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="d8327-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8327-109">EXAMPLES</span></span>

### <span data-ttu-id="d8327-110">Exempel 1: skapa en privat länk konfiguration med en enda IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="d8327-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="d8327-111">Det här kommandot skapar en PrivateLink-konfiguration med namnet "privateLinkConfig01" och lagrar resultatet i variabeln som heter $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d8327-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="d8327-112">Exempel 2: skapa en privat länk-konfiguration med flera IP-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="d8327-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="d8327-113">Det här kommandot skapar en PrivateLink-konfiguration med namnet "privateLinkConfig01" med två ipConfigurations och lagrar resultatet i variabeln som heter $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d8327-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="d8327-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8327-114">PARAMETERS</span></span>

### <span data-ttu-id="d8327-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8327-115">-DefaultProfile</span></span>
<span data-ttu-id="d8327-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8327-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8327-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8327-117">-IpConfiguration</span></span>
<span data-ttu-id="d8327-118">Listan över ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8327-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8327-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8327-119">-Name</span></span>
<span data-ttu-id="d8327-120">Namnet på privateLink-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d8327-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="d8327-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8327-121">-Confirm</span></span>
<span data-ttu-id="d8327-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8327-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8327-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8327-123">-WhatIf</span></span>
<span data-ttu-id="d8327-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8327-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8327-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8327-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8327-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8327-126">CommonParameters</span></span>
<span data-ttu-id="d8327-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8327-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8327-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8327-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8327-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8327-129">INPUTS</span></span>

### <span data-ttu-id="d8327-130">Microsoft. Azure. commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="d8327-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="d8327-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8327-131">OUTPUTS</span></span>

### <span data-ttu-id="d8327-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8327-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="d8327-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8327-133">NOTES</span></span>

## <span data-ttu-id="d8327-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8327-134">RELATED LINKS</span></span>

[<span data-ttu-id="d8327-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8327-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d8327-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8327-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d8327-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8327-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d8327-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8327-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
