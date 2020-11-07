---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 1196480735705186ad3493b6c34a473baf35dc0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920063"
---
# <span data-ttu-id="eeb24-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="eeb24-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="eeb24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eeb24-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb24-103">Tar bort en användare från en AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="eeb24-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="eeb24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eeb24-104">SYNTAX</span></span>

### <span data-ttu-id="eeb24-105">ExplicitParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="eeb24-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eeb24-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="eeb24-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb24-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="eeb24-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb24-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="eeb24-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb24-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeb24-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb24-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeb24-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb24-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeb24-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb24-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eeb24-112">DESCRIPTION</span></span>
<span data-ttu-id="eeb24-113">Tar bort en användare från en AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="eeb24-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="eeb24-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eeb24-114">EXAMPLES</span></span>

### <span data-ttu-id="eeb24-115">Exempel 1 – ta bort en användare från en grupp efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="eeb24-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="eeb24-116">Tar bort användaren med objekt-ID ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' från gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="eeb24-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="eeb24-117">Exempel 2 – ta bort en användare från en grupp efter ledning</span><span class="sxs-lookup"><span data-stu-id="eeb24-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="eeb24-118">Hämtar gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och rör den till Remove-AzADGroupMember cmdlet för att ta bort användaren till gruppen.</span><span class="sxs-lookup"><span data-stu-id="eeb24-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="eeb24-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eeb24-119">PARAMETERS</span></span>

### <span data-ttu-id="eeb24-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb24-120">-DefaultProfile</span></span>
<span data-ttu-id="eeb24-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eeb24-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeb24-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="eeb24-122">-GroupDisplayName</span></span>
<span data-ttu-id="eeb24-123">Visnings namnet på gruppen som du vill ta bort medlemmen/medlemmarna från.</span><span class="sxs-lookup"><span data-stu-id="eeb24-123">The display name of the group to remove the member(s) from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb24-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="eeb24-124">-GroupObject</span></span>
<span data-ttu-id="eeb24-125">Objekt representation för gruppen som medlemmen ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="eeb24-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb24-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="eeb24-126">-GroupObjectId</span></span>
<span data-ttu-id="eeb24-127">Objekt-ID för gruppen som medlemmen ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="eeb24-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb24-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="eeb24-128">-MemberObjectId</span></span>
<span data-ttu-id="eeb24-129">Objekt-ID för medlemmen.</span><span class="sxs-lookup"><span data-stu-id="eeb24-129">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb24-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="eeb24-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="eeb24-131">UPN för de medlemmar som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="eeb24-131">The UPN of the member(s) to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb24-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eeb24-132">-PassThru</span></span>
<span data-ttu-id="eeb24-133">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="eeb24-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="eeb24-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eeb24-134">-Confirm</span></span>
<span data-ttu-id="eeb24-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eeb24-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb24-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb24-136">-WhatIf</span></span>
<span data-ttu-id="eeb24-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eeb24-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb24-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eeb24-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb24-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb24-139">CommonParameters</span></span>
<span data-ttu-id="eeb24-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb24-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb24-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb24-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb24-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eeb24-142">INPUTS</span></span>

### <span data-ttu-id="eeb24-143">Microsoft. Azure. commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="eeb24-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="eeb24-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eeb24-144">OUTPUTS</span></span>

### <span data-ttu-id="eeb24-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eeb24-145">System.Boolean</span></span>

## <span data-ttu-id="eeb24-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eeb24-146">NOTES</span></span>

## <span data-ttu-id="eeb24-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eeb24-147">RELATED LINKS</span></span>
