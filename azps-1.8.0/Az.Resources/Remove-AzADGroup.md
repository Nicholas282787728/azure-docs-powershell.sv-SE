---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: f4c8a4fb3f10f7a019df95e82d7bbd3ad469411c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747083"
---
# <span data-ttu-id="f1d50-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="f1d50-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="f1d50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1d50-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d50-103">Tar bort en Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="f1d50-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="f1d50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1d50-104">SYNTAX</span></span>

### <span data-ttu-id="f1d50-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f1d50-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d50-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1d50-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d50-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1d50-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1d50-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1d50-108">DESCRIPTION</span></span>
<span data-ttu-id="f1d50-109">Tar bort en Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="f1d50-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="f1d50-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1d50-110">EXAMPLES</span></span>

### <span data-ttu-id="f1d50-111">Exempel 1 – ta bort en grupp efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="f1d50-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="f1d50-112">Tar bort gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="f1d50-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="f1d50-113">Exempel 2 – ta bort en grupp efter rör</span><span class="sxs-lookup"><span data-stu-id="f1d50-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="f1d50-114">Hämtar gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och pipes för att Remove-AzADGroup ta bort gruppen från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="f1d50-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="f1d50-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1d50-115">PARAMETERS</span></span>

### <span data-ttu-id="f1d50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d50-116">-DefaultProfile</span></span>
<span data-ttu-id="f1d50-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f1d50-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1d50-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f1d50-118">-DisplayName</span></span>
<span data-ttu-id="f1d50-119">Visnings namnet på gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f1d50-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d50-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f1d50-120">-Force</span></span>
<span data-ttu-id="f1d50-121">Om det anges ber vi dig bekräfta att du vill ta bort gruppen.</span><span class="sxs-lookup"><span data-stu-id="f1d50-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d50-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1d50-122">-InputObject</span></span>
<span data-ttu-id="f1d50-123">Objekt representation för gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f1d50-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d50-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f1d50-124">-ObjectId</span></span>
<span data-ttu-id="f1d50-125">Objekt-ID för gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f1d50-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d50-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1d50-126">-PassThru</span></span>
<span data-ttu-id="f1d50-127">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="f1d50-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d50-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f1d50-128">-Confirm</span></span>
<span data-ttu-id="f1d50-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1d50-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1d50-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1d50-130">-WhatIf</span></span>
<span data-ttu-id="f1d50-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f1d50-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1d50-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f1d50-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1d50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d50-133">CommonParameters</span></span>
<span data-ttu-id="f1d50-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1d50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d50-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1d50-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d50-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1d50-136">INPUTS</span></span>

### <span data-ttu-id="f1d50-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f1d50-137">System.String</span></span>

### <span data-ttu-id="f1d50-138">Microsoft. Azure. commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="f1d50-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="f1d50-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1d50-139">OUTPUTS</span></span>

### <span data-ttu-id="f1d50-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1d50-140">System.Boolean</span></span>

## <span data-ttu-id="f1d50-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1d50-141">NOTES</span></span>

## <span data-ttu-id="f1d50-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1d50-142">RELATED LINKS</span></span>
