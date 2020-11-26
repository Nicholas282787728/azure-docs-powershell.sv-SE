---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270929"
---
# <span data-ttu-id="22348-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="22348-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="22348-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22348-102">SYNOPSIS</span></span>
<span data-ttu-id="22348-103">Tillämpa underhålls uppdateringar för resursen</span><span class="sxs-lookup"><span data-stu-id="22348-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="22348-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22348-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22348-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22348-105">DESCRIPTION</span></span>
<span data-ttu-id="22348-106">Tillämpa underhålls uppdateringar för resursen</span><span class="sxs-lookup"><span data-stu-id="22348-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="22348-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22348-107">EXAMPLES</span></span>

### <span data-ttu-id="22348-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="22348-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="22348-109">Tillämpa underhålls uppdateringar för resursen</span><span class="sxs-lookup"><span data-stu-id="22348-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="22348-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22348-110">PARAMETERS</span></span>

### <span data-ttu-id="22348-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22348-111">-AsJob</span></span>
<span data-ttu-id="22348-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="22348-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22348-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22348-113">-DefaultProfile</span></span>
<span data-ttu-id="22348-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22348-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22348-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="22348-115">-ProviderName</span></span>
<span data-ttu-id="22348-116">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="22348-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="22348-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22348-117">-ResourceGroupName</span></span>
<span data-ttu-id="22348-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="22348-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="22348-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="22348-119">-ResourceName</span></span>
<span data-ttu-id="22348-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="22348-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22348-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="22348-121">-ResourceParentName</span></span>
<span data-ttu-id="22348-122">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="22348-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22348-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="22348-123">-ResourceParentType</span></span>
<span data-ttu-id="22348-124">Den överordnade resurs typen.</span><span class="sxs-lookup"><span data-stu-id="22348-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22348-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="22348-125">-ResourceType</span></span>
<span data-ttu-id="22348-126">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="22348-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22348-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22348-127">-Confirm</span></span>
<span data-ttu-id="22348-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22348-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22348-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22348-129">-WhatIf</span></span>
<span data-ttu-id="22348-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22348-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22348-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22348-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22348-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22348-132">CommonParameters</span></span>
<span data-ttu-id="22348-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22348-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22348-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22348-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22348-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22348-135">INPUTS</span></span>

### <span data-ttu-id="22348-136">System. String</span><span class="sxs-lookup"><span data-stu-id="22348-136">System.String</span></span>

## <span data-ttu-id="22348-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22348-137">OUTPUTS</span></span>

### <span data-ttu-id="22348-138">Microsoft. Azure. commands. Maintenance. Models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="22348-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="22348-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22348-139">NOTES</span></span>

## <span data-ttu-id="22348-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22348-140">RELATED LINKS</span></span>