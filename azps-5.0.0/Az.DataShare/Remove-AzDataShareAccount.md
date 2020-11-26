---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 0e8c3fac1c286845686d158c01217b0d4199639c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320279"
---
# <span data-ttu-id="ad302-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="ad302-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="ad302-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad302-102">SYNOPSIS</span></span>
<span data-ttu-id="ad302-103">Tar bort ett datashare-konto</span><span class="sxs-lookup"><span data-stu-id="ad302-103">Removes a datashare account</span></span>

## <span data-ttu-id="ad302-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad302-104">SYNTAX</span></span>

### <span data-ttu-id="ad302-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ad302-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad302-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad302-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad302-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad302-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad302-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad302-108">DESCRIPTION</span></span>
<span data-ttu-id="ad302-109">Cmdleten **Remove-AzDataShareAccount** tar bort ett datashare-konto.</span><span class="sxs-lookup"><span data-stu-id="ad302-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="ad302-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad302-110">EXAMPLES</span></span>

### <span data-ttu-id="ad302-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ad302-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="ad302-112">Det här kommandot tar bort datashare-kontot som heter WikiADS från resurs gruppen annonser.</span><span class="sxs-lookup"><span data-stu-id="ad302-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="ad302-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="ad302-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="ad302-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad302-114">PARAMETERS</span></span>

### <span data-ttu-id="ad302-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad302-115">-AsJob</span></span>
<span data-ttu-id="ad302-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="ad302-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="ad302-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad302-117">-DefaultProfile</span></span>
<span data-ttu-id="ad302-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad302-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad302-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ad302-119">-Force</span></span>
<span data-ttu-id="ad302-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="ad302-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="ad302-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad302-121">-InputObject</span></span>
<span data-ttu-id="ad302-122">Objekt för Azure Data Share-kontot.</span><span class="sxs-lookup"><span data-stu-id="ad302-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad302-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad302-123">-Name</span></span>
<span data-ttu-id="ad302-124">Namn på Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="ad302-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="ad302-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad302-125">-PassThru</span></span>
<span data-ttu-id="ad302-126">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="ad302-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="ad302-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad302-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad302-128">Resurs grupp namnet för Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="ad302-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="ad302-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad302-129">-ResourceId</span></span>
<span data-ttu-id="ad302-130">Resurs-ID för Azure Data Share-kontot.</span><span class="sxs-lookup"><span data-stu-id="ad302-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="ad302-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad302-131">-Confirm</span></span>
<span data-ttu-id="ad302-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad302-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad302-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad302-133">-WhatIf</span></span>
<span data-ttu-id="ad302-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad302-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad302-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad302-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad302-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad302-136">CommonParameters</span></span>
<span data-ttu-id="ad302-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad302-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad302-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad302-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad302-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad302-139">INPUTS</span></span>

### <span data-ttu-id="ad302-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ad302-140">System.String</span></span>

### <span data-ttu-id="ad302-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="ad302-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="ad302-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad302-142">OUTPUTS</span></span>

### <span data-ttu-id="ad302-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad302-143">System.Boolean</span></span>

## <span data-ttu-id="ad302-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad302-144">NOTES</span></span>

## <span data-ttu-id="ad302-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad302-145">RELATED LINKS</span></span>