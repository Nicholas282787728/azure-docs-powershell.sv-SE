---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 82fdec48f2e021e33490f84a05a064fb007ac8d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574895"
---
# <span data-ttu-id="f9c81-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9c81-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="f9c81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9c81-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c81-103">Skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="f9c81-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9c81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9c81-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9c81-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9c81-105">DESCRIPTION</span></span>
<span data-ttu-id="f9c81-106">Cmdleten **New-AzureRmApplicationSecurityGroup** skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="f9c81-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="f9c81-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9c81-107">EXAMPLES</span></span>

### <span data-ttu-id="f9c81-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f9c81-108">Example 1</span></span>
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="f9c81-109">I det här exemplet skapas en säkerhets grupp för program utan associationer.</span><span class="sxs-lookup"><span data-stu-id="f9c81-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="f9c81-110">När det har skapats kan IP-konfigurationer i nätverks gränssnittet ingå i gruppen.</span><span class="sxs-lookup"><span data-stu-id="f9c81-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="f9c81-111">Säkerhets reglerna kan även referera till gruppen som deras källor eller destinationer.</span><span class="sxs-lookup"><span data-stu-id="f9c81-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="f9c81-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9c81-112">PARAMETERS</span></span>

### <span data-ttu-id="f9c81-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9c81-113">-AsJob</span></span>
<span data-ttu-id="f9c81-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f9c81-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9c81-115">-DefaultProfile</span></span>
<span data-ttu-id="f9c81-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9c81-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9c81-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f9c81-117">-Force</span></span>
<span data-ttu-id="f9c81-118">Fråga inte efter bekräftelse om du vill skriva över en resurs.</span><span class="sxs-lookup"><span data-stu-id="f9c81-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c81-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="f9c81-119">-Location</span></span>
<span data-ttu-id="f9c81-120">Platsen.</span><span class="sxs-lookup"><span data-stu-id="f9c81-120">The location.</span></span>

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

### <span data-ttu-id="f9c81-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f9c81-121">-Name</span></span>
<span data-ttu-id="f9c81-122">Namnet på program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="f9c81-122">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c81-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9c81-123">-ResourceGroupName</span></span>
<span data-ttu-id="f9c81-124">Resurs grupps namnet för program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="f9c81-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="f9c81-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f9c81-125">-Tag</span></span>
<span data-ttu-id="f9c81-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="f9c81-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c81-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f9c81-127">-Confirm</span></span>
<span data-ttu-id="f9c81-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f9c81-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9c81-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9c81-129">-WhatIf</span></span>
<span data-ttu-id="f9c81-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f9c81-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9c81-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f9c81-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9c81-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c81-132">CommonParameters</span></span>
<span data-ttu-id="f9c81-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9c81-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c81-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9c81-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c81-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9c81-135">INPUTS</span></span>

### <span data-ttu-id="f9c81-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f9c81-136">System.String</span></span>
<span data-ttu-id="f9c81-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f9c81-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f9c81-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9c81-138">OUTPUTS</span></span>

### <span data-ttu-id="f9c81-139">Microsoft. Azure. commands. Networks. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9c81-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="f9c81-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9c81-140">NOTES</span></span>

## <span data-ttu-id="f9c81-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9c81-141">RELATED LINKS</span></span>

[<span data-ttu-id="f9c81-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9c81-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="f9c81-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9c81-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="f9c81-144">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9c81-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f9c81-145">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9c81-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f9c81-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9c81-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f9c81-147">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9c81-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f9c81-148">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9c81-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f9c81-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9c81-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)