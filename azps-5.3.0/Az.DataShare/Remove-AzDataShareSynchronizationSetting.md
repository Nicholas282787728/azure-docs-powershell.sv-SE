---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420547"
---
# <span data-ttu-id="4f208-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="4f208-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="4f208-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f208-102">SYNOPSIS</span></span>
<span data-ttu-id="4f208-103">tar bort en synkronisering</span><span class="sxs-lookup"><span data-stu-id="4f208-103">removes a synchronization setting</span></span>

## <span data-ttu-id="4f208-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f208-104">SYNTAX</span></span>

### <span data-ttu-id="4f208-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4f208-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f208-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f208-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f208-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f208-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f208-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f208-108">DESCRIPTION</span></span>
<span data-ttu-id="4f208-109">Cmdleten **Remove-AzDataShareSynchronizationSetting** tar bort synkroniseringsinställningarna för datashare</span><span class="sxs-lookup"><span data-stu-id="4f208-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="4f208-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f208-110">EXAMPLES</span></span>

### <span data-ttu-id="4f208-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f208-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4f208-112">Med det här kommandot tas en synkroniseringsresurs bort som heter AdsShareSynchronizationSetting från Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="4f208-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="4f208-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f208-113">PARAMETERS</span></span>

### <span data-ttu-id="4f208-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4f208-114">-AccountName</span></span>
<span data-ttu-id="4f208-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="4f208-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="4f208-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f208-116">-AsJob</span></span>
<span data-ttu-id="4f208-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="4f208-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="4f208-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f208-118">-DefaultProfile</span></span>
<span data-ttu-id="4f208-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f208-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f208-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f208-120">-InputObject</span></span>
<span data-ttu-id="4f208-121">Inställningen för synkronisering av Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="4f208-121">The Azure Data Share Synchronization setting.</span></span>


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

### <span data-ttu-id="4f208-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f208-122">-Name</span></span>
<span data-ttu-id="4f208-123">Inställnings namn för synkronisering</span><span class="sxs-lookup"><span data-stu-id="4f208-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="4f208-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f208-124">-PassThru</span></span>
<span data-ttu-id="4f208-125">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="4f208-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="4f208-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f208-126">-ResourceGroupName</span></span>
<span data-ttu-id="4f208-127">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="4f208-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4f208-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f208-128">-ResourceId</span></span>
<span data-ttu-id="4f208-129">Resurs-ID för synkroniseringsinställningarna</span><span class="sxs-lookup"><span data-stu-id="4f208-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="4f208-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4f208-130">-ShareName</span></span>
<span data-ttu-id="4f208-131">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="4f208-131">Azure data share name</span></span>

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

### <span data-ttu-id="4f208-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f208-132">-Confirm</span></span>
<span data-ttu-id="4f208-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f208-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f208-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f208-134">-WhatIf</span></span>
<span data-ttu-id="4f208-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f208-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f208-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f208-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f208-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f208-137">CommonParameters</span></span>
<span data-ttu-id="4f208-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f208-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f208-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f208-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f208-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f208-140">INPUTS</span></span>

### <span data-ttu-id="4f208-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4f208-141">System.String</span></span>

### <span data-ttu-id="4f208-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="4f208-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="4f208-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f208-143">OUTPUTS</span></span>

### <span data-ttu-id="4f208-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f208-144">System.Boolean</span></span>

## <span data-ttu-id="4f208-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f208-145">NOTES</span></span>

## <span data-ttu-id="4f208-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f208-146">RELATED LINKS</span></span>
