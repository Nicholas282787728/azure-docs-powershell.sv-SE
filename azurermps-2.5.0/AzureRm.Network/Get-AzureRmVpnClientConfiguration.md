---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
ms.openlocfilehash: 4d6e95534cdadd694fa2ed87d43d3f7387ec9b20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929350"
---
# <span data-ttu-id="5cf5a-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cf5a-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="5cf5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cf5a-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf5a-103">Gör det enkelt att ladda ned VPN-profilen som genererades med New-AzureRmVpnClientConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5cf5a-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cf5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cf5a-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cf5a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cf5a-105">DESCRIPTION</span></span>
<span data-ttu-id="5cf5a-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="5cf5a-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="5cf5a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cf5a-107">EXAMPLES</span></span>

### <span data-ttu-id="5cf5a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5cf5a-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="5cf5a-109">Hämtar URL-adressen för att hämta en VpnClient-profil som tidigare genererats med kommandot New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5cf5a-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="5cf5a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cf5a-110">PARAMETERS</span></span>

### <span data-ttu-id="5cf5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf5a-111">-DefaultProfile</span></span>
<span data-ttu-id="5cf5a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf5a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="5cf5a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="5cf5a-113">-Name</span></span>
<span data-ttu-id="5cf5a-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="5cf5a-114">The resource name.</span></span>

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

### <span data-ttu-id="5cf5a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf5a-115">-ResourceGroupName</span></span>
<span data-ttu-id="5cf5a-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5cf5a-116">The resource group name.</span></span>

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

### <span data-ttu-id="5cf5a-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5cf5a-117">-Confirm</span></span>
<span data-ttu-id="5cf5a-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5cf5a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cf5a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cf5a-119">-WhatIf</span></span>
<span data-ttu-id="5cf5a-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5cf5a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cf5a-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5cf5a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cf5a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf5a-122">CommonParameters</span></span>
<span data-ttu-id="5cf5a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf5a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf5a-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf5a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf5a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cf5a-125">INPUTS</span></span>

### <span data-ttu-id="5cf5a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf5a-126">System.String</span></span>

## <span data-ttu-id="5cf5a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cf5a-127">OUTPUTS</span></span>

### <span data-ttu-id="5cf5a-128">Microsoft. Azure. commands. Networks. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="5cf5a-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="5cf5a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cf5a-129">NOTES</span></span>

## <span data-ttu-id="5cf5a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cf5a-130">RELATED LINKS</span></span>

