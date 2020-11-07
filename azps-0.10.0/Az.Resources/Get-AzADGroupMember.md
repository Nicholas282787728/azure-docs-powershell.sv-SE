---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: f083498860f3f2b9e19280b41d953032796e0eb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924058"
---
# <span data-ttu-id="bf2fc-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="bf2fc-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="bf2fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf2fc-102">SYNOPSIS</span></span>
<span data-ttu-id="bf2fc-103">Visar medlemmar i en AD-grupp i den aktuella innehavaren.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="bf2fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf2fc-104">SYNTAX</span></span>

### <span data-ttu-id="bf2fc-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bf2fc-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bf2fc-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf2fc-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bf2fc-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf2fc-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="bf2fc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf2fc-108">DESCRIPTION</span></span>
<span data-ttu-id="bf2fc-109">Visar medlemmar i en AD-grupp i den aktuella innehavaren.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="bf2fc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf2fc-110">EXAMPLES</span></span>

### <span data-ttu-id="bf2fc-111">Exempel 1 – Visa medlemmar efter AD-gruppobjekt-ID</span><span class="sxs-lookup"><span data-stu-id="bf2fc-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="bf2fc-112">Visar medlemmar i AD-gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="bf2fc-113">Exempel 2 – Visa medlemmar efter AD-gruppobjekt-ID med sid indelning</span><span class="sxs-lookup"><span data-stu-id="bf2fc-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="bf2fc-114">Visar de första 100 medlemmarna i AD-gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="bf2fc-115">Exempel 3 – Visa medlemmar efter ledning</span><span class="sxs-lookup"><span data-stu-id="bf2fc-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="bf2fc-116">Hämtar AD-gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och kopplar den till Get-AzADGroupMember cmdlet för att lista alla medlemmar i gruppen.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="bf2fc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf2fc-117">PARAMETERS</span></span>

### <span data-ttu-id="bf2fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf2fc-118">-DefaultProfile</span></span>
<span data-ttu-id="bf2fc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bf2fc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf2fc-120">-Först</span><span class="sxs-lookup"><span data-stu-id="bf2fc-120">-First</span></span>
<span data-ttu-id="bf2fc-121">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-121">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf2fc-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="bf2fc-122">-GroupDisplayName</span></span>
<span data-ttu-id="bf2fc-123">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-123">The display name of the group.</span></span>

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

### <span data-ttu-id="bf2fc-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="bf2fc-124">-GroupObject</span></span>
<span data-ttu-id="bf2fc-125">Gruppobjektet som du visar medlemmar från.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-125">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf2fc-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="bf2fc-126">-GroupObjectId</span></span>
<span data-ttu-id="bf2fc-127">Objekt-ID för gruppen.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-127">Object Id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf2fc-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="bf2fc-128">-IncludeTotalCount</span></span>
<span data-ttu-id="bf2fc-129">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="bf2fc-130">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="bf2fc-131">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="bf2fc-131">-Skip</span></span>
<span data-ttu-id="bf2fc-132">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-132">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf2fc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf2fc-133">CommonParameters</span></span>
<span data-ttu-id="bf2fc-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf2fc-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf2fc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf2fc-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf2fc-136">INPUTS</span></span>

### <span data-ttu-id="bf2fc-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bf2fc-137">System.Guid</span></span>

### <span data-ttu-id="bf2fc-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="bf2fc-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="bf2fc-139">Parametrar: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf2fc-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="bf2fc-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf2fc-140">OUTPUTS</span></span>

### <span data-ttu-id="bf2fc-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="bf2fc-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="bf2fc-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf2fc-142">NOTES</span></span>

## <span data-ttu-id="bf2fc-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf2fc-143">RELATED LINKS</span></span>

[<span data-ttu-id="bf2fc-144">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="bf2fc-144">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="bf2fc-145">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bf2fc-145">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

