---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 069705ffc119fae964e931164f97bfbae72eca35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924077"
---
# <span data-ttu-id="e9938-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="e9938-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="e9938-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9938-102">SYNOPSIS</span></span>
<span data-ttu-id="e9938-103">Lägger till en användare i en befintlig AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="e9938-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="e9938-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9938-104">SYNTAX</span></span>

### <span data-ttu-id="e9938-105">MemberObjectIdWithGroupObjectId (standard)</span><span class="sxs-lookup"><span data-stu-id="e9938-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9938-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="e9938-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9938-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="e9938-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9938-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9938-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9938-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9938-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9938-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9938-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9938-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9938-111">DESCRIPTION</span></span>
<span data-ttu-id="e9938-112">Lägger till en användare i en befintlig AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="e9938-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="e9938-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9938-113">EXAMPLES</span></span>

### <span data-ttu-id="e9938-114">Exempel 1 – Lägg till en användare i en grupp efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="e9938-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="e9938-115">Lägger till användaren med objekt-ID ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' i gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="e9938-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="e9938-116">Exempel 2 – Lägg till en användare i en grupp efter ledning</span><span class="sxs-lookup"><span data-stu-id="e9938-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="e9938-117">Hämtar gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och rör den till Add-AzADGroupMember cmdlet för att lägga till användaren i gruppen.</span><span class="sxs-lookup"><span data-stu-id="e9938-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="e9938-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9938-118">PARAMETERS</span></span>

### <span data-ttu-id="e9938-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9938-119">-DefaultProfile</span></span>
<span data-ttu-id="e9938-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9938-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9938-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="e9938-121">-MemberObjectId</span></span>
<span data-ttu-id="e9938-122">Objekt-ID för medlemmen.</span><span class="sxs-lookup"><span data-stu-id="e9938-122">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9938-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e9938-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="e9938-124">UPN för den eller de medlemmar som ska läggas till i gruppen.</span><span class="sxs-lookup"><span data-stu-id="e9938-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="e9938-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9938-125">-PassThru</span></span>
<span data-ttu-id="e9938-126">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="e9938-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e9938-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="e9938-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="e9938-128">Visnings namnet på gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="e9938-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="e9938-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="e9938-129">-TargetGroupObject</span></span>
<span data-ttu-id="e9938-130">Objekt representation för gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="e9938-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="e9938-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="e9938-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="e9938-132">Objekt-ID för gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="e9938-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="e9938-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9938-133">-Confirm</span></span>
<span data-ttu-id="e9938-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9938-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9938-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9938-135">-WhatIf</span></span>
<span data-ttu-id="e9938-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e9938-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9938-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e9938-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9938-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9938-138">CommonParameters</span></span>
<span data-ttu-id="e9938-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9938-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9938-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9938-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9938-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9938-141">INPUTS</span></span>

### <span data-ttu-id="e9938-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="e9938-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="e9938-143">Parametrar: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e9938-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="e9938-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9938-144">OUTPUTS</span></span>

### <span data-ttu-id="e9938-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9938-145">System.Boolean</span></span>

## <span data-ttu-id="e9938-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9938-146">NOTES</span></span>

## <span data-ttu-id="e9938-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9938-147">RELATED LINKS</span></span>
