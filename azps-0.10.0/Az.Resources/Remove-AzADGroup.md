---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 4d285471632c9c4bc952b2dcdc0e4ce5147fac12
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923882"
---
# <span data-ttu-id="dafea-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="dafea-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="dafea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dafea-102">SYNOPSIS</span></span>
<span data-ttu-id="dafea-103">Tar bort en Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="dafea-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="dafea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dafea-104">SYNTAX</span></span>

### <span data-ttu-id="dafea-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dafea-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dafea-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dafea-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dafea-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dafea-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dafea-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dafea-108">DESCRIPTION</span></span>
<span data-ttu-id="dafea-109">Tar bort en Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="dafea-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="dafea-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dafea-110">EXAMPLES</span></span>

### <span data-ttu-id="dafea-111">Exempel 1 – ta bort en grupp efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="dafea-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="dafea-112">Tar bort gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="dafea-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="dafea-113">Exempel 2 – ta bort en grupp efter rör</span><span class="sxs-lookup"><span data-stu-id="dafea-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="dafea-114">Hämtar gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och pipes för att Remove-AzADGroup ta bort gruppen från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="dafea-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="dafea-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dafea-115">PARAMETERS</span></span>

### <span data-ttu-id="dafea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafea-116">-DefaultProfile</span></span>
<span data-ttu-id="dafea-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dafea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dafea-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dafea-118">-DisplayName</span></span>
<span data-ttu-id="dafea-119">Visnings namnet på gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="dafea-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="dafea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dafea-120">-Force</span></span>
<span data-ttu-id="dafea-121">Om det anges ber vi dig bekräfta att du vill ta bort gruppen.</span><span class="sxs-lookup"><span data-stu-id="dafea-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="dafea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dafea-122">-InputObject</span></span>
<span data-ttu-id="dafea-123">Objekt representation för gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="dafea-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dafea-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dafea-124">-ObjectId</span></span>
<span data-ttu-id="dafea-125">Objekt-ID för gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="dafea-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dafea-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dafea-126">-PassThru</span></span>
<span data-ttu-id="dafea-127">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="dafea-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="dafea-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dafea-128">-Confirm</span></span>
<span data-ttu-id="dafea-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dafea-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dafea-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dafea-130">-WhatIf</span></span>
<span data-ttu-id="dafea-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dafea-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dafea-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dafea-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dafea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafea-133">CommonParameters</span></span>
<span data-ttu-id="dafea-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dafea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafea-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dafea-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafea-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dafea-136">INPUTS</span></span>

### <span data-ttu-id="dafea-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="dafea-137">System.Guid</span></span>

### <span data-ttu-id="dafea-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="dafea-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="dafea-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dafea-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="dafea-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dafea-140">OUTPUTS</span></span>

### <span data-ttu-id="dafea-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dafea-141">System.Boolean</span></span>

## <span data-ttu-id="dafea-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dafea-142">NOTES</span></span>

## <span data-ttu-id="dafea-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dafea-143">RELATED LINKS</span></span>
