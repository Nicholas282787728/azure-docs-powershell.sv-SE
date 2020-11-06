---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 9ab4af1eefa6214d43eca84f65053eeecb12d912
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576228"
---
# <span data-ttu-id="cda37-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="cda37-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="cda37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cda37-102">SYNOPSIS</span></span>
<span data-ttu-id="cda37-103">Gör det enkelt att ladda ned VPN-profilen som genererades med New-AzureRmVpnClientConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cda37-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cda37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cda37-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cda37-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cda37-105">DESCRIPTION</span></span>
<span data-ttu-id="cda37-106">Get-AzureRmVpnClientConfiguration returnerar URL-adressen där VPN-klienten kan laddas ned från.</span><span class="sxs-lookup"><span data-stu-id="cda37-106">The Get-AzureRmVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="cda37-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cda37-107">EXAMPLES</span></span>

### <span data-ttu-id="cda37-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cda37-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="cda37-109">Hämtar URL-adressen för att hämta en VpnClient-profil som tidigare genererats med kommandot New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cda37-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="cda37-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cda37-110">PARAMETERS</span></span>

### <span data-ttu-id="cda37-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda37-111">-DefaultProfile</span></span>
<span data-ttu-id="cda37-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cda37-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cda37-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="cda37-113">-Name</span></span>
<span data-ttu-id="cda37-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="cda37-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda37-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda37-115">-ResourceGroupName</span></span>
<span data-ttu-id="cda37-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cda37-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda37-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cda37-117">-Confirm</span></span>
<span data-ttu-id="cda37-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cda37-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda37-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda37-119">-WhatIf</span></span>
<span data-ttu-id="cda37-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cda37-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cda37-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cda37-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda37-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda37-122">CommonParameters</span></span>
<span data-ttu-id="cda37-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda37-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda37-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cda37-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda37-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cda37-125">INPUTS</span></span>

### <span data-ttu-id="cda37-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cda37-126">System.String</span></span>

## <span data-ttu-id="cda37-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cda37-127">OUTPUTS</span></span>

### <span data-ttu-id="cda37-128">Microsoft. Azure. commands. Networks. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="cda37-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="cda37-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cda37-129">NOTES</span></span>

## <span data-ttu-id="cda37-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cda37-130">RELATED LINKS</span></span>
