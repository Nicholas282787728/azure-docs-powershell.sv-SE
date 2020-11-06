---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/add-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
ms.openlocfilehash: 333a56a59c28482c2da228e3e9c0f8c2f1c21f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575122"
---
# <span data-ttu-id="37dee-101">Add-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="37dee-101">Add-AzureRmADGroupMember</span></span>

## <span data-ttu-id="37dee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37dee-102">SYNOPSIS</span></span>
<span data-ttu-id="37dee-103">Lägger till en användare i en befintlig AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="37dee-103">Adds a user to an existing AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37dee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37dee-104">SYNTAX</span></span>

### <span data-ttu-id="37dee-105">MemberObjectIdWithGroupObjectId (standard)</span><span class="sxs-lookup"><span data-stu-id="37dee-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37dee-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="37dee-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37dee-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="37dee-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37dee-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="37dee-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37dee-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37dee-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37dee-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37dee-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37dee-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37dee-111">DESCRIPTION</span></span>
<span data-ttu-id="37dee-112">Lägger till en användare i en befintlig AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="37dee-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="37dee-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37dee-113">EXAMPLES</span></span>

### <span data-ttu-id="37dee-114">Exempel 1 – Lägg till en användare i en grupp efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="37dee-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="37dee-115">Lägger till användaren med objekt-ID ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' i gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="37dee-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="37dee-116">Exempel 2 – Lägg till en användare i en grupp efter ledning</span><span class="sxs-lookup"><span data-stu-id="37dee-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="37dee-117">Hämtar gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och rör den till Add-AzureRmADGroupMember cmdlet för att lägga till användaren i gruppen.</span><span class="sxs-lookup"><span data-stu-id="37dee-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzureRmADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="37dee-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37dee-118">PARAMETERS</span></span>

### <span data-ttu-id="37dee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37dee-119">-DefaultProfile</span></span>
<span data-ttu-id="37dee-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37dee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37dee-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="37dee-121">-MemberObjectId</span></span>
<span data-ttu-id="37dee-122">Objekt-ID för medlemmen.</span><span class="sxs-lookup"><span data-stu-id="37dee-122">The object id of the member.</span></span>

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

### <span data-ttu-id="37dee-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="37dee-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="37dee-124">UPN för den eller de medlemmar som ska läggas till i gruppen.</span><span class="sxs-lookup"><span data-stu-id="37dee-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="37dee-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37dee-125">-PassThru</span></span>
<span data-ttu-id="37dee-126">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="37dee-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="37dee-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="37dee-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="37dee-128">Visnings namnet på gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="37dee-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="37dee-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="37dee-129">-TargetGroupObject</span></span>
<span data-ttu-id="37dee-130">Objekt representation för gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="37dee-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="37dee-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="37dee-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="37dee-132">Objekt-ID för gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="37dee-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="37dee-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37dee-133">-Confirm</span></span>
<span data-ttu-id="37dee-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37dee-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37dee-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37dee-135">-WhatIf</span></span>
<span data-ttu-id="37dee-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37dee-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37dee-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37dee-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37dee-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dee-138">CommonParameters</span></span>
<span data-ttu-id="37dee-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37dee-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dee-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37dee-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dee-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37dee-141">INPUTS</span></span>

### <span data-ttu-id="37dee-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="37dee-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="37dee-143">Parametrar: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="37dee-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="37dee-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37dee-144">OUTPUTS</span></span>

### <span data-ttu-id="37dee-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37dee-145">System.Boolean</span></span>

## <span data-ttu-id="37dee-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37dee-146">NOTES</span></span>

## <span data-ttu-id="37dee-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37dee-147">RELATED LINKS</span></span>
