---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
ms.openlocfilehash: 515591660abf34399caa5643c05478fd4295141a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755682"
---
# <span data-ttu-id="74d46-101">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="74d46-101">Remove-AzureRmADGroupMember</span></span>

## <span data-ttu-id="74d46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74d46-102">SYNOPSIS</span></span>
<span data-ttu-id="74d46-103">Tar bort en användare från en AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="74d46-103">Removes a user from an AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74d46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74d46-104">SYNTAX</span></span>

### <span data-ttu-id="74d46-105">ExplicitParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="74d46-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzureRmADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74d46-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="74d46-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d46-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="74d46-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d46-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="74d46-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d46-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d46-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d46-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d46-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d46-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d46-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74d46-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74d46-112">DESCRIPTION</span></span>
<span data-ttu-id="74d46-113">Tar bort en användare från en AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="74d46-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="74d46-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74d46-114">EXAMPLES</span></span>

### <span data-ttu-id="74d46-115">Exempel 1 – ta bort en användare från en grupp efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="74d46-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="74d46-116">Tar bort användaren med objekt-ID ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' från gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="74d46-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="74d46-117">Exempel 2 – ta bort en användare från en grupp efter ledning</span><span class="sxs-lookup"><span data-stu-id="74d46-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="74d46-118">Hämtar gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och rör den till Remove-AzureRmADGroupMember cmdlet för att ta bort användaren till gruppen.</span><span class="sxs-lookup"><span data-stu-id="74d46-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzureRmADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="74d46-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74d46-119">PARAMETERS</span></span>

### <span data-ttu-id="74d46-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d46-120">-DefaultProfile</span></span>
<span data-ttu-id="74d46-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74d46-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d46-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="74d46-122">-GroupDisplayName</span></span>
<span data-ttu-id="74d46-123">Visnings namnet på gruppen som du vill ta bort medlemmen/medlemmarna från.</span><span class="sxs-lookup"><span data-stu-id="74d46-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="74d46-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="74d46-124">-GroupObject</span></span>
<span data-ttu-id="74d46-125">Objekt representation för gruppen som medlemmen ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="74d46-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74d46-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="74d46-126">-GroupObjectId</span></span>
<span data-ttu-id="74d46-127">Objekt-ID för gruppen som medlemmen ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="74d46-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d46-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="74d46-128">-MemberObjectId</span></span>
<span data-ttu-id="74d46-129">Objekt-ID för medlemmen.</span><span class="sxs-lookup"><span data-stu-id="74d46-129">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d46-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="74d46-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="74d46-131">UPN för de medlemmar som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="74d46-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="74d46-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74d46-132">-PassThru</span></span>
<span data-ttu-id="74d46-133">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="74d46-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="74d46-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74d46-134">-Confirm</span></span>
<span data-ttu-id="74d46-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74d46-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d46-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d46-136">-WhatIf</span></span>
<span data-ttu-id="74d46-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74d46-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74d46-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74d46-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d46-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d46-139">CommonParameters</span></span>
<span data-ttu-id="74d46-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d46-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d46-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74d46-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d46-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74d46-142">INPUTS</span></span>

### <span data-ttu-id="74d46-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="74d46-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="74d46-144">Parametrar: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74d46-144">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="74d46-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74d46-145">OUTPUTS</span></span>

### <span data-ttu-id="74d46-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74d46-146">System.Boolean</span></span>

## <span data-ttu-id="74d46-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74d46-147">NOTES</span></span>

## <span data-ttu-id="74d46-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74d46-148">RELATED LINKS</span></span>
