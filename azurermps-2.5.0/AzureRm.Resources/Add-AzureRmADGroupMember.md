---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/add-azurermadgroupmember
schema: 2.0.0
ms.openlocfilehash: 4f1949a80d16ddbbd22584c314a01785ed9a393d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929234"
---
# <span data-ttu-id="95287-101">Add-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="95287-101">Add-AzureRmADGroupMember</span></span>

## <span data-ttu-id="95287-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95287-102">SYNOPSIS</span></span>
<span data-ttu-id="95287-103">Lägger till en användare i en befintlig AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="95287-103">Adds a user to an existing AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95287-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95287-104">SYNTAX</span></span>

### <span data-ttu-id="95287-105">MemberObjectIdWithGroupObjectId (standard)</span><span class="sxs-lookup"><span data-stu-id="95287-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95287-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="95287-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95287-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="95287-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95287-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="95287-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95287-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95287-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95287-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95287-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95287-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95287-111">DESCRIPTION</span></span>
<span data-ttu-id="95287-112">Lägger till en användare i en befintlig AD-grupp.</span><span class="sxs-lookup"><span data-stu-id="95287-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="95287-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95287-113">EXAMPLES</span></span>

### <span data-ttu-id="95287-114">Exempel 1 – Lägg till en användare i en grupp efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="95287-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="95287-115">Lägger till användaren med objekt-ID ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' i gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="95287-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="95287-116">Exempel 2 – Lägg till en användare i en grupp efter ledning</span><span class="sxs-lookup"><span data-stu-id="95287-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="95287-117">Hämtar gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och rör den till Add-AzureRmADGroupMember cmdlet för att lägga till användaren i gruppen.</span><span class="sxs-lookup"><span data-stu-id="95287-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzureRmADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="95287-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95287-118">PARAMETERS</span></span>

### <span data-ttu-id="95287-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95287-119">-DefaultProfile</span></span>
<span data-ttu-id="95287-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95287-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95287-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="95287-121">-MemberObjectId</span></span>
<span data-ttu-id="95287-122">Objekt-ID för medlemmen.</span><span class="sxs-lookup"><span data-stu-id="95287-122">The object id of the member.</span></span>

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

### <span data-ttu-id="95287-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="95287-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="95287-124">UPN för den eller de medlemmar som ska läggas till i gruppen.</span><span class="sxs-lookup"><span data-stu-id="95287-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="95287-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95287-125">-PassThru</span></span>
<span data-ttu-id="95287-126">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="95287-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="95287-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="95287-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="95287-128">Visnings namnet på gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="95287-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="95287-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="95287-129">-TargetGroupObject</span></span>
<span data-ttu-id="95287-130">Objekt representation för gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="95287-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="95287-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="95287-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="95287-132">Objekt-ID för gruppen som du vill lägga till medlemmar i.</span><span class="sxs-lookup"><span data-stu-id="95287-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="95287-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="95287-133">-Confirm</span></span>
<span data-ttu-id="95287-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95287-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95287-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95287-135">-WhatIf</span></span>
<span data-ttu-id="95287-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="95287-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95287-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="95287-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95287-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95287-138">CommonParameters</span></span>
<span data-ttu-id="95287-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95287-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95287-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95287-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95287-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95287-141">INPUTS</span></span>

### <span data-ttu-id="95287-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="95287-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="95287-143">Parametrar: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95287-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="95287-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95287-144">OUTPUTS</span></span>

### <span data-ttu-id="95287-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95287-145">System.Boolean</span></span>

## <span data-ttu-id="95287-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95287-146">NOTES</span></span>

## <span data-ttu-id="95287-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95287-147">RELATED LINKS</span></span>
