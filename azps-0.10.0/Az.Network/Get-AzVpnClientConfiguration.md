---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 63b044c4a9736aca72e9713cd8ec5833e7b056ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922201"
---
# <span data-ttu-id="96c54-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c54-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="96c54-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96c54-102">SYNOPSIS</span></span>
<span data-ttu-id="96c54-103">Gör det enkelt att ladda ned VPN-profilen som genererades med New-AzVpnClientConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96c54-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="96c54-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96c54-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96c54-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96c54-105">DESCRIPTION</span></span>
<span data-ttu-id="96c54-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="96c54-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="96c54-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96c54-107">EXAMPLES</span></span>

### <span data-ttu-id="96c54-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="96c54-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="96c54-109">Hämtar URL-adressen för att hämta en VpnClient-profil som tidigare genererats med kommandot New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="96c54-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="96c54-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96c54-110">PARAMETERS</span></span>

### <span data-ttu-id="96c54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c54-111">-DefaultProfile</span></span>
<span data-ttu-id="96c54-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96c54-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="96c54-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="96c54-113">-Name</span></span>
<span data-ttu-id="96c54-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="96c54-114">The resource name.</span></span>

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

### <span data-ttu-id="96c54-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c54-115">-ResourceGroupName</span></span>
<span data-ttu-id="96c54-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="96c54-116">The resource group name.</span></span>

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

### <span data-ttu-id="96c54-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96c54-117">-Confirm</span></span>
<span data-ttu-id="96c54-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96c54-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c54-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c54-119">-WhatIf</span></span>
<span data-ttu-id="96c54-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96c54-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96c54-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96c54-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c54-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c54-122">CommonParameters</span></span>
<span data-ttu-id="96c54-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c54-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c54-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c54-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c54-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96c54-125">INPUTS</span></span>

### <span data-ttu-id="96c54-126">System. String</span><span class="sxs-lookup"><span data-stu-id="96c54-126">System.String</span></span>

## <span data-ttu-id="96c54-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96c54-127">OUTPUTS</span></span>

### <span data-ttu-id="96c54-128">Microsoft. Azure. commands. Networks. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="96c54-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="96c54-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96c54-129">NOTES</span></span>

## <span data-ttu-id="96c54-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96c54-130">RELATED LINKS</span></span>

