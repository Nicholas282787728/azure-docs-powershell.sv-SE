---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: ffc04a6b1560845a0c29db4d000270fe91aa8ff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586308"
---
# <span data-ttu-id="b3e80-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="b3e80-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="b3e80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3e80-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e80-103">Visar medlemmar i en AD-grupp i den aktuella innehavaren.</span><span class="sxs-lookup"><span data-stu-id="b3e80-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3e80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3e80-104">SYNTAX</span></span>

### <span data-ttu-id="b3e80-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b3e80-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b3e80-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3e80-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b3e80-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3e80-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="b3e80-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3e80-108">DESCRIPTION</span></span>
<span data-ttu-id="b3e80-109">Visar medlemmar i en AD-grupp i den aktuella innehavaren.</span><span class="sxs-lookup"><span data-stu-id="b3e80-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="b3e80-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3e80-110">EXAMPLES</span></span>

### <span data-ttu-id="b3e80-111">Exempel 1 – Visa medlemmar efter AD-gruppobjekt-ID</span><span class="sxs-lookup"><span data-stu-id="b3e80-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="b3e80-112">Visar medlemmar i AD-gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="b3e80-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="b3e80-113">Exempel 2 – Visa medlemmar efter AD-gruppobjekt-ID med sid indelning</span><span class="sxs-lookup"><span data-stu-id="b3e80-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="b3e80-114">Visar de första 100 medlemmarna i AD-gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="b3e80-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="b3e80-115">Exempel 3 – Visa medlemmar efter ledning</span><span class="sxs-lookup"><span data-stu-id="b3e80-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="b3e80-116">Hämtar AD-gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och kopplar den till Get-AzureRmADGroupMember cmdlet för att lista alla medlemmar i gruppen.</span><span class="sxs-lookup"><span data-stu-id="b3e80-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="b3e80-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3e80-117">PARAMETERS</span></span>

### <span data-ttu-id="b3e80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e80-118">-DefaultProfile</span></span>
<span data-ttu-id="b3e80-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b3e80-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3e80-120">-Först</span><span class="sxs-lookup"><span data-stu-id="b3e80-120">-First</span></span>
<span data-ttu-id="b3e80-121">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="b3e80-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="b3e80-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="b3e80-122">-GroupDisplayName</span></span>
<span data-ttu-id="b3e80-123">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="b3e80-123">The display name of the group.</span></span>

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

### <span data-ttu-id="b3e80-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="b3e80-124">-GroupObject</span></span>
<span data-ttu-id="b3e80-125">Gruppobjektet som du visar medlemmar från.</span><span class="sxs-lookup"><span data-stu-id="b3e80-125">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="b3e80-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="b3e80-126">-GroupObjectId</span></span>
<span data-ttu-id="b3e80-127">Objekt-ID för gruppen.</span><span class="sxs-lookup"><span data-stu-id="b3e80-127">Object Id of the group.</span></span>

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

### <span data-ttu-id="b3e80-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="b3e80-128">-IncludeTotalCount</span></span>
<span data-ttu-id="b3e80-129">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="b3e80-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="b3e80-130">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="b3e80-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="b3e80-131">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="b3e80-131">-Skip</span></span>
<span data-ttu-id="b3e80-132">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="b3e80-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="b3e80-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e80-133">CommonParameters</span></span>
<span data-ttu-id="b3e80-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e80-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e80-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e80-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e80-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3e80-136">INPUTS</span></span>

### <span data-ttu-id="b3e80-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b3e80-137">System.Guid</span></span>

### <span data-ttu-id="b3e80-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="b3e80-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="b3e80-139">Parametrar: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b3e80-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="b3e80-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3e80-140">OUTPUTS</span></span>

### <span data-ttu-id="b3e80-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="b3e80-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="b3e80-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3e80-142">NOTES</span></span>

## <span data-ttu-id="b3e80-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3e80-143">RELATED LINKS</span></span>

[<span data-ttu-id="b3e80-144">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b3e80-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="b3e80-145">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b3e80-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

