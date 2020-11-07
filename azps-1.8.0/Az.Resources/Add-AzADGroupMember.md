---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 876bc41e1faf1d830a247a56f9917f22023e5a6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747191"
---
# <span data-ttu-id="39bfc-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="39bfc-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="39bfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="39bfc-103">Lägger till en användare i en befintlig AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="39bfc-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="39bfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39bfc-104">SYNTAX</span></span>

### <span data-ttu-id="39bfc-105">MemberObjectIdWithGroupObjectId (standard)</span><span class="sxs-lookup"><span data-stu-id="39bfc-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39bfc-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="39bfc-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39bfc-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="39bfc-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39bfc-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="39bfc-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39bfc-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39bfc-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39bfc-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39bfc-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39bfc-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39bfc-111">DESCRIPTION</span></span>
<span data-ttu-id="39bfc-112">Lägger till en användare i en befintlig AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="39bfc-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="39bfc-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39bfc-113">EXAMPLES</span></span>

### <span data-ttu-id="39bfc-114">Exempel 1 – Lägg till en användare i en grupp efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="39bfc-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="39bfc-115">Lägger till användaren med objekt-ID ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' i gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="39bfc-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="39bfc-116">Exempel 2 – Lägg till en användare i en grupp efter ledning</span><span class="sxs-lookup"><span data-stu-id="39bfc-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="39bfc-117">Hämtar gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och rör den till Add-AzADGroupMember cmdlet för att lägga till användaren i gruppen.</span><span class="sxs-lookup"><span data-stu-id="39bfc-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="39bfc-118">Exempel 3 – Lägg till en användare i en grupp efter huvud namn</span><span class="sxs-lookup"><span data-stu-id="39bfc-118">Example 3 - Add a user to a group by principal name</span></span>

```
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="39bfc-119">Lägger till en användare i en grupp och visar medlemmar i gruppen.</span><span class="sxs-lookup"><span data-stu-id="39bfc-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="39bfc-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39bfc-120">PARAMETERS</span></span>

### <span data-ttu-id="39bfc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39bfc-121">-DefaultProfile</span></span>
<span data-ttu-id="39bfc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39bfc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39bfc-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="39bfc-123">-MemberObjectId</span></span>
<span data-ttu-id="39bfc-124">Objekt-ID för medlemmen.</span><span class="sxs-lookup"><span data-stu-id="39bfc-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bfc-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="39bfc-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="39bfc-126">UPN för den eller de medlemmar som ska läggas till i gruppen.</span><span class="sxs-lookup"><span data-stu-id="39bfc-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="39bfc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39bfc-127">-PassThru</span></span>
<span data-ttu-id="39bfc-128">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="39bfc-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="39bfc-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="39bfc-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="39bfc-130">Visnings namnet på gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="39bfc-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="39bfc-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="39bfc-131">-TargetGroupObject</span></span>
<span data-ttu-id="39bfc-132">Objekt representation för gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="39bfc-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="39bfc-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="39bfc-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="39bfc-134">Objekt-ID för gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="39bfc-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="39bfc-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39bfc-135">-Confirm</span></span>
<span data-ttu-id="39bfc-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39bfc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39bfc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39bfc-137">-WhatIf</span></span>
<span data-ttu-id="39bfc-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39bfc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39bfc-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39bfc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39bfc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39bfc-140">CommonParameters</span></span>
<span data-ttu-id="39bfc-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39bfc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39bfc-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39bfc-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39bfc-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39bfc-143">INPUTS</span></span>

### <span data-ttu-id="39bfc-144">Microsoft. Azure. commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="39bfc-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="39bfc-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39bfc-145">OUTPUTS</span></span>

### <span data-ttu-id="39bfc-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39bfc-146">System.Boolean</span></span>

## <span data-ttu-id="39bfc-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39bfc-147">NOTES</span></span>

## <span data-ttu-id="39bfc-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39bfc-148">RELATED LINKS</span></span>