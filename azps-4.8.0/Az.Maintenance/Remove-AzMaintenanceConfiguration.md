---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259365"
---
# <span data-ttu-id="0bc5b-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0bc5b-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="0bc5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0bc5b-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc5b-103">Ta bort konfigurations post</span><span class="sxs-lookup"><span data-stu-id="0bc5b-103">Delete Configuration record</span></span>

## <span data-ttu-id="0bc5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0bc5b-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bc5b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0bc5b-105">DESCRIPTION</span></span>
<span data-ttu-id="0bc5b-106">Ta bort underhålls konfigurations post</span><span class="sxs-lookup"><span data-stu-id="0bc5b-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="0bc5b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0bc5b-107">EXAMPLES</span></span>

### <span data-ttu-id="0bc5b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0bc5b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="0bc5b-109">Ta bort underhålls konfigurations post</span><span class="sxs-lookup"><span data-stu-id="0bc5b-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="0bc5b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0bc5b-110">PARAMETERS</span></span>

### <span data-ttu-id="0bc5b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bc5b-111">-AsJob</span></span>
<span data-ttu-id="0bc5b-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0bc5b-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bc5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc5b-113">-DefaultProfile</span></span>
<span data-ttu-id="0bc5b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bc5b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0bc5b-115">-Force</span></span>
<span data-ttu-id="0bc5b-116">Tvinga bort utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-116">Force remove without confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bc5b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="0bc5b-117">-Name</span></span>
<span data-ttu-id="0bc5b-118">Konfigurations namn för underhåll.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-118">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc5b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bc5b-119">-PassThru</span></span>
<span data-ttu-id="0bc5b-120">Returnerar statusen för Remove-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="0bc5b-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bc5b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc5b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0bc5b-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-123">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc5b-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0bc5b-124">-Confirm</span></span>
<span data-ttu-id="0bc5b-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bc5b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bc5b-126">-WhatIf</span></span>
<span data-ttu-id="0bc5b-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bc5b-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bc5b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc5b-129">CommonParameters</span></span>
<span data-ttu-id="0bc5b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc5b-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bc5b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc5b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0bc5b-132">INPUTS</span></span>

### <span data-ttu-id="0bc5b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0bc5b-133">System.String</span></span>

## <span data-ttu-id="0bc5b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0bc5b-134">OUTPUTS</span></span>

### <span data-ttu-id="0bc5b-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0bc5b-135">System.Boolean</span></span>

## <span data-ttu-id="0bc5b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0bc5b-136">NOTES</span></span>

## <span data-ttu-id="0bc5b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0bc5b-137">RELATED LINKS</span></span>