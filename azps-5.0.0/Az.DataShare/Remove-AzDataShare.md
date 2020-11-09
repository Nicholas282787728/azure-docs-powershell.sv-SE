---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320280"
---
# <span data-ttu-id="7ac11-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="7ac11-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="7ac11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ac11-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac11-103">Tar bort en data resurs.</span><span class="sxs-lookup"><span data-stu-id="7ac11-103">Removes a data share.</span></span>

## <span data-ttu-id="7ac11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ac11-104">SYNTAX</span></span>

### <span data-ttu-id="7ac11-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7ac11-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac11-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ac11-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac11-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ac11-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ac11-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ac11-108">DESCRIPTION</span></span>
<span data-ttu-id="7ac11-109">Cmdleten **Remove-AzDataShare** tar bort en data resurs.</span><span class="sxs-lookup"><span data-stu-id="7ac11-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="7ac11-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ac11-110">EXAMPLES</span></span>

### <span data-ttu-id="7ac11-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ac11-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="7ac11-112">De här kommandona tar bort data resursen som heter AdsShare från WikiAds för Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="7ac11-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="7ac11-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ac11-113">PARAMETERS</span></span>

### <span data-ttu-id="7ac11-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7ac11-114">-AccountName</span></span>
<span data-ttu-id="7ac11-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="7ac11-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ac11-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ac11-116">-AsJob</span></span>
<span data-ttu-id="7ac11-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="7ac11-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="7ac11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac11-118">-DefaultProfile</span></span>
<span data-ttu-id="7ac11-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac11-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ac11-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ac11-120">-InputObject</span></span>
<span data-ttu-id="7ac11-121">Azure Data Share-objekt ' ' ' yaml typ: PSDataShare parameter uppsättningar: ByObjectParameterSet alias:</span><span class="sxs-lookup"><span data-stu-id="7ac11-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="7ac11-122">Obligatoriskt: sant position: namngivet standardvärde: ingen acceptera pipeline-inmatning: sant (ByValue) acceptera jokertecken: falskt</span><span class="sxs-lookup"><span data-stu-id="7ac11-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac11-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ac11-123">-Name</span></span>
<span data-ttu-id="7ac11-124">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="7ac11-124">Azure data share name</span></span>

<span data-ttu-id="7ac11-125">yaml typ: sträng parameter uppsättningar: ByFieldsParameterSet-alias:</span><span class="sxs-lookup"><span data-stu-id="7ac11-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="7ac11-126">Obligatoriskt: sant position: namngivet standardvärde: ingen acceptera pipeline-inmatning: falskt acceptera jokertecken: falskt</span><span class="sxs-lookup"><span data-stu-id="7ac11-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ac11-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ac11-127">-PassThru</span></span>
<span data-ttu-id="7ac11-128">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="7ac11-128">Return object (if specified).</span></span>

<span data-ttu-id="7ac11-129">yaml typ: SwitchParameter parameter uppsättningar: (alla) alias:</span><span class="sxs-lookup"><span data-stu-id="7ac11-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="7ac11-130">Obligatoriskt: falskt position: namngivet standardvärde: ingen acceptera pipeline-inmatning: falskt acceptera jokertecken: falskt</span><span class="sxs-lookup"><span data-stu-id="7ac11-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="7ac11-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ac11-131">-ResourceGroupName</span></span>
<span data-ttu-id="7ac11-132">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="7ac11-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="7ac11-133">yaml typ: sträng parameter uppsättningar: ByFieldsParameterSet-alias:</span><span class="sxs-lookup"><span data-stu-id="7ac11-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="7ac11-134">Obligatoriskt: sant position: namngivet standardvärde: ingen acceptera pipeline-inmatning: falskt acceptera jokertecken: falskt</span><span class="sxs-lookup"><span data-stu-id="7ac11-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ac11-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ac11-135">-ResourceId</span></span>
<span data-ttu-id="7ac11-136">Resurs-ID för Azure Data-resursen</span><span class="sxs-lookup"><span data-stu-id="7ac11-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="7ac11-137">yaml typ: sträng parameter uppsättningar: ByResourceIdParameterSet-alias:</span><span class="sxs-lookup"><span data-stu-id="7ac11-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="7ac11-138">Obligatoriskt: sant position: namngivet standardvärde: ingen acceptera pipeline-inmatning: sant (ByPropertyName) acceptera jokertecken: falskt</span><span class="sxs-lookup"><span data-stu-id="7ac11-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac11-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ac11-139">-Confirm</span></span>
<span data-ttu-id="7ac11-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ac11-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="7ac11-141">yaml typ: SwitchParameter parameter uppsättningar: (alla) alias: CF</span><span class="sxs-lookup"><span data-stu-id="7ac11-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="7ac11-142">Obligatoriskt: falskt position: namngivet standardvärde: ingen acceptera pipeline-inmatning: falskt acceptera jokertecken: falskt</span><span class="sxs-lookup"><span data-stu-id="7ac11-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="7ac11-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac11-143">-WhatIf</span></span>
<span data-ttu-id="7ac11-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ac11-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ac11-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ac11-145">The cmdlet is not run.</span></span>

<span data-ttu-id="7ac11-146">yaml typ: SwitchParameter parameter uppsättningar: (alla) alias: trådlöst</span><span class="sxs-lookup"><span data-stu-id="7ac11-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="7ac11-147">Obligatoriskt: falskt position: namngivet standardvärde: ingen acceptera pipeline-inmatning: falskt acceptera jokertecken: falskt</span><span class="sxs-lookup"><span data-stu-id="7ac11-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="7ac11-148">yaml typ: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare parameter uppsättningar: ByObjectParameterSet alias:</span><span class="sxs-lookup"><span data-stu-id="7ac11-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="7ac11-149">Obligatoriskt: sant position: namngivet standardvärde: ingen acceptera pipeline-inmatning: sant (ByValue) acceptera jokertecken: falskt</span><span class="sxs-lookup"><span data-stu-id="7ac11-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="7ac11-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac11-150">CommonParameters</span></span>
<span data-ttu-id="7ac11-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac11-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac11-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ac11-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac11-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ac11-153">INPUTS</span></span>

### <span data-ttu-id="7ac11-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7ac11-154">System.String</span></span>

### <span data-ttu-id="7ac11-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="7ac11-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="7ac11-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ac11-156">OUTPUTS</span></span>

### <span data-ttu-id="7ac11-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ac11-157">System.Boolean</span></span>

## <span data-ttu-id="7ac11-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ac11-158">NOTES</span></span>

## <span data-ttu-id="7ac11-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ac11-159">RELATED LINKS</span></span>
