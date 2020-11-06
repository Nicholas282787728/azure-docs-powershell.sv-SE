---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 09c3862513b893003908b07992ae479656ba7ab1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586028"
---
# <span data-ttu-id="326dc-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="326dc-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="326dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="326dc-102">SYNOPSIS</span></span>
<span data-ttu-id="326dc-103">Gör det enkelt att ladda ned VPN-profilen som genererades med New-AzureRmVpnClientConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="326dc-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="326dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="326dc-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="326dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="326dc-105">DESCRIPTION</span></span>
<span data-ttu-id="326dc-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="326dc-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="326dc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="326dc-107">EXAMPLES</span></span>

### <span data-ttu-id="326dc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="326dc-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="326dc-109">Hämtar URL-adressen för att hämta en VpnClient-profil som tidigare genererats med kommandot New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="326dc-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="326dc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="326dc-110">PARAMETERS</span></span>

### <span data-ttu-id="326dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326dc-111">-DefaultProfile</span></span>
<span data-ttu-id="326dc-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="326dc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="326dc-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="326dc-113">-Name</span></span>
<span data-ttu-id="326dc-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="326dc-114">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="326dc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="326dc-115">-ResourceGroupName</span></span>
<span data-ttu-id="326dc-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="326dc-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="326dc-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="326dc-117">-Confirm</span></span>
<span data-ttu-id="326dc-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="326dc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="326dc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="326dc-119">-WhatIf</span></span>
<span data-ttu-id="326dc-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="326dc-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="326dc-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="326dc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="326dc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326dc-122">CommonParameters</span></span>
<span data-ttu-id="326dc-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="326dc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326dc-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="326dc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326dc-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="326dc-125">INPUTS</span></span>

### <span data-ttu-id="326dc-126">System. String</span><span class="sxs-lookup"><span data-stu-id="326dc-126">System.String</span></span>

## <span data-ttu-id="326dc-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="326dc-127">OUTPUTS</span></span>

### <span data-ttu-id="326dc-128">Microsoft. Azure. commands. Networks. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="326dc-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="326dc-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="326dc-129">NOTES</span></span>

## <span data-ttu-id="326dc-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="326dc-130">RELATED LINKS</span></span>

