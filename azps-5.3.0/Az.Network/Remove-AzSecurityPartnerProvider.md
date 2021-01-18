---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523825"
---
# <span data-ttu-id="09ebc-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="09ebc-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="09ebc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="09ebc-103">Tar bort en Azure-SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="09ebc-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="09ebc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09ebc-104">SYNTAX</span></span>

### <span data-ttu-id="09ebc-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09ebc-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09ebc-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09ebc-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09ebc-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09ebc-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09ebc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09ebc-108">DESCRIPTION</span></span>
<span data-ttu-id="09ebc-109">Cmdleten **Remove-AzSecurityPartnerProvider** tar bort en Azure-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="09ebc-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="09ebc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09ebc-110">EXAMPLES</span></span>

### <span data-ttu-id="09ebc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="09ebc-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="09ebc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09ebc-112">PARAMETERS</span></span>

### <span data-ttu-id="09ebc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09ebc-113">-AsJob</span></span>
<span data-ttu-id="09ebc-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="09ebc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09ebc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ebc-115">-DefaultProfile</span></span>
<span data-ttu-id="09ebc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09ebc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09ebc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="09ebc-117">-Force</span></span>
<span data-ttu-id="09ebc-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="09ebc-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="09ebc-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="09ebc-119">-Name</span></span>
<span data-ttu-id="09ebc-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="09ebc-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ebc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09ebc-121">-PassThru</span></span>
<span data-ttu-id="09ebc-122">Returnerar ett objekt som representerar objektet som den här åtgärden utförs på.</span><span class="sxs-lookup"><span data-stu-id="09ebc-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="09ebc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ebc-123">-ResourceGroupName</span></span>
<span data-ttu-id="09ebc-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="09ebc-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ebc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09ebc-125">-ResourceId</span></span>
<span data-ttu-id="09ebc-126">Resurs-ID för securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="09ebc-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ebc-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="09ebc-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="09ebc-128">SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="09ebc-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09ebc-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09ebc-129">-Confirm</span></span>
<span data-ttu-id="09ebc-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09ebc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09ebc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09ebc-131">-WhatIf</span></span>
<span data-ttu-id="09ebc-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09ebc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09ebc-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09ebc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09ebc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ebc-134">CommonParameters</span></span>
<span data-ttu-id="09ebc-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ebc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ebc-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09ebc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ebc-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09ebc-137">INPUTS</span></span>

### <span data-ttu-id="09ebc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="09ebc-138">System.String</span></span>

### <span data-ttu-id="09ebc-139">Microsoft. Azure. commands. Networks. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="09ebc-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="09ebc-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09ebc-140">OUTPUTS</span></span>

### <span data-ttu-id="09ebc-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09ebc-141">System.Boolean</span></span>

## <span data-ttu-id="09ebc-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09ebc-142">NOTES</span></span>

## <span data-ttu-id="09ebc-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09ebc-143">RELATED LINKS</span></span>
