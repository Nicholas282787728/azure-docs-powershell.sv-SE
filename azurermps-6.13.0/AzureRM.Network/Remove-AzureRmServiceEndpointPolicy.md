---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: f3871e23c0d193ef2ea89c43e3a30c5597abbfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584088"
---
# <span data-ttu-id="5254a-101">Remove-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5254a-101">Remove-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="5254a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5254a-102">SYNOPSIS</span></span>
<span data-ttu-id="5254a-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="5254a-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5254a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5254a-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5254a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5254a-105">DESCRIPTION</span></span>
<span data-ttu-id="5254a-106">Cmdleten **Remove-AzureRmServiceEndpointPolicy** tar bort en princip för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="5254a-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="5254a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5254a-107">EXAMPLES</span></span>

### <span data-ttu-id="5254a-108">Exempel 1: tar bort en princip för service slut punkter med namn</span><span class="sxs-lookup"><span data-stu-id="5254a-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="5254a-109">Det här kommandot tar bort en tjänst slut punkts princip med namnet Policy1 som tillhör resourcegroup med namnet "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="5254a-109">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="5254a-110">Exempel 2: ta bort en policy för tjänst slut punkter med hjälp av indata</span><span class="sxs-lookup"><span data-stu-id="5254a-110">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzureRmServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="5254a-111">Det här kommandot tar bort ett princip objekt för service Endpoint Policy1 som tillhör resourcegroup med namnet "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="5254a-111">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="5254a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5254a-112">PARAMETERS</span></span>

### <span data-ttu-id="5254a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5254a-113">-DefaultProfile</span></span>
<span data-ttu-id="5254a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5254a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5254a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5254a-115">-Force</span></span>
<span data-ttu-id="5254a-116">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="5254a-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="5254a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5254a-117">-Name</span></span>
<span data-ttu-id="5254a-118">Namnet på tjänstens slut punkts princip</span><span class="sxs-lookup"><span data-stu-id="5254a-118">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="5254a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5254a-119">-PassThru</span></span>
<span data-ttu-id="5254a-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5254a-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5254a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5254a-121">-ResourceGroupName</span></span>
<span data-ttu-id="5254a-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5254a-122">The resource group name.</span></span>

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

### <span data-ttu-id="5254a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5254a-123">-Confirm</span></span>
<span data-ttu-id="5254a-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5254a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5254a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5254a-125">-WhatIf</span></span>
<span data-ttu-id="5254a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5254a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5254a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5254a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5254a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5254a-128">CommonParameters</span></span>
<span data-ttu-id="5254a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5254a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5254a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5254a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5254a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5254a-131">INPUTS</span></span>

### <span data-ttu-id="5254a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5254a-132">System.String</span></span>


## <span data-ttu-id="5254a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5254a-133">OUTPUTS</span></span>

### <span data-ttu-id="5254a-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="5254a-134">System.Object</span></span>

## <span data-ttu-id="5254a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5254a-135">NOTES</span></span>

## <span data-ttu-id="5254a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5254a-136">RELATED LINKS</span></span>
