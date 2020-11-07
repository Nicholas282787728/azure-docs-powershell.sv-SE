---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 0ff167f14c9a831cb2afe2ce335a0c8bcd18acc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744411"
---
# <span data-ttu-id="ba07a-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="ba07a-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="ba07a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba07a-102">SYNOPSIS</span></span>
<span data-ttu-id="ba07a-103">tar bort en synkronisering</span><span class="sxs-lookup"><span data-stu-id="ba07a-103">removes a synchronization setting</span></span>

## <span data-ttu-id="ba07a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba07a-104">SYNTAX</span></span>

### <span data-ttu-id="ba07a-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ba07a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba07a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba07a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba07a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba07a-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba07a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba07a-108">DESCRIPTION</span></span>
<span data-ttu-id="ba07a-109">Cmdleten **Remove-AzDataShareSynchronizationSetting** tar bort synkroniseringsinställningarna för datashare</span><span class="sxs-lookup"><span data-stu-id="ba07a-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="ba07a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba07a-110">EXAMPLES</span></span>

### <span data-ttu-id="ba07a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ba07a-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="ba07a-112">Med det här kommandot tas en synkroniseringsresurs bort som heter AdsShareSynchronizationSetting från Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="ba07a-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="ba07a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba07a-113">PARAMETERS</span></span>

### <span data-ttu-id="ba07a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ba07a-114">-AccountName</span></span>
<span data-ttu-id="ba07a-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="ba07a-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="ba07a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba07a-116">-AsJob</span></span>
<span data-ttu-id="ba07a-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="ba07a-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="ba07a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba07a-118">-DefaultProfile</span></span>
<span data-ttu-id="ba07a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba07a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba07a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba07a-120">-InputObject</span></span>
<span data-ttu-id="ba07a-121">Inställningen för synkronisering av Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="ba07a-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba07a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba07a-122">-Name</span></span>
<span data-ttu-id="ba07a-123">Inställnings namn för synkronisering</span><span class="sxs-lookup"><span data-stu-id="ba07a-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="ba07a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba07a-124">-PassThru</span></span>
<span data-ttu-id="ba07a-125">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="ba07a-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="ba07a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba07a-126">-ResourceGroupName</span></span>
<span data-ttu-id="ba07a-127">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="ba07a-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ba07a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba07a-128">-ResourceId</span></span>
<span data-ttu-id="ba07a-129">Resurs-ID för synkroniseringsinställningarna</span><span class="sxs-lookup"><span data-stu-id="ba07a-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="ba07a-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ba07a-130">-ShareName</span></span>
<span data-ttu-id="ba07a-131">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="ba07a-131">Azure data share name</span></span>

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

### <span data-ttu-id="ba07a-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ba07a-132">-Confirm</span></span>
<span data-ttu-id="ba07a-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ba07a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba07a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba07a-134">-WhatIf</span></span>
<span data-ttu-id="ba07a-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ba07a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba07a-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ba07a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba07a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba07a-137">CommonParameters</span></span>
<span data-ttu-id="ba07a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba07a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba07a-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba07a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba07a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba07a-140">INPUTS</span></span>

### <span data-ttu-id="ba07a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ba07a-141">System.String</span></span>

### <span data-ttu-id="ba07a-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="ba07a-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="ba07a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba07a-143">OUTPUTS</span></span>

### <span data-ttu-id="ba07a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba07a-144">System.Boolean</span></span>

## <span data-ttu-id="ba07a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba07a-145">NOTES</span></span>

## <span data-ttu-id="ba07a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba07a-146">RELATED LINKS</span></span>
