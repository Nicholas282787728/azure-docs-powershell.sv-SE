---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 25de035b853d1a17ee06a7efb6ac31631bd466f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747179"
---
# <span data-ttu-id="ddce9-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="ddce9-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="ddce9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddce9-102">SYNOPSIS</span></span>
<span data-ttu-id="ddce9-103">Visar medlemmar i en AD-grupp i den aktuella innehavaren.</span><span class="sxs-lookup"><span data-stu-id="ddce9-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="ddce9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddce9-104">SYNTAX</span></span>

### <span data-ttu-id="ddce9-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ddce9-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ddce9-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddce9-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ddce9-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddce9-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="ddce9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddce9-108">DESCRIPTION</span></span>
<span data-ttu-id="ddce9-109">Visar medlemmar i en AD-grupp i den aktuella innehavaren.</span><span class="sxs-lookup"><span data-stu-id="ddce9-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="ddce9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddce9-110">EXAMPLES</span></span>

### <span data-ttu-id="ddce9-111">Exempel 1 – Visa medlemmar efter AD-gruppobjekt-ID</span><span class="sxs-lookup"><span data-stu-id="ddce9-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="ddce9-112">Visar medlemmar i AD-gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="ddce9-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="ddce9-113">Exempel 2 – Visa medlemmar efter AD-gruppobjekt-ID med sid indelning</span><span class="sxs-lookup"><span data-stu-id="ddce9-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="ddce9-114">Visar de första 100 medlemmarna i AD-gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="ddce9-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="ddce9-115">Exempel 3 – Visa medlemmar efter ledning</span><span class="sxs-lookup"><span data-stu-id="ddce9-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="ddce9-116">Hämtar AD-gruppen med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' och kopplar den till Get-AzADGroupMember cmdlet för att lista alla medlemmar i gruppen.</span><span class="sxs-lookup"><span data-stu-id="ddce9-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="ddce9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddce9-117">PARAMETERS</span></span>

### <span data-ttu-id="ddce9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddce9-118">-DefaultProfile</span></span>
<span data-ttu-id="ddce9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ddce9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddce9-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="ddce9-120">-GroupDisplayName</span></span>
<span data-ttu-id="ddce9-121">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="ddce9-121">The display name of the group.</span></span>

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

### <span data-ttu-id="ddce9-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="ddce9-122">-GroupObject</span></span>
<span data-ttu-id="ddce9-123">Gruppobjektet som du visar medlemmar från.</span><span class="sxs-lookup"><span data-stu-id="ddce9-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddce9-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="ddce9-124">-GroupObjectId</span></span>
<span data-ttu-id="ddce9-125">Objekt-ID för gruppen.</span><span class="sxs-lookup"><span data-stu-id="ddce9-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddce9-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="ddce9-126">-IncludeTotalCount</span></span>
<span data-ttu-id="ddce9-127">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddce9-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="ddce9-128">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="ddce9-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="ddce9-129">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="ddce9-129">-Skip</span></span>
<span data-ttu-id="ddce9-130">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="ddce9-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="ddce9-131">-Först</span><span class="sxs-lookup"><span data-stu-id="ddce9-131">-First</span></span>
<span data-ttu-id="ddce9-132">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="ddce9-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="ddce9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddce9-133">CommonParameters</span></span>
<span data-ttu-id="ddce9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddce9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddce9-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddce9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddce9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddce9-136">INPUTS</span></span>

### <span data-ttu-id="ddce9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ddce9-137">System.String</span></span>

### <span data-ttu-id="ddce9-138">Microsoft. Azure. commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="ddce9-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="ddce9-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddce9-139">OUTPUTS</span></span>

### <span data-ttu-id="ddce9-140">Microsoft. Azure. commands. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="ddce9-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="ddce9-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddce9-141">NOTES</span></span>

## <span data-ttu-id="ddce9-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddce9-142">RELATED LINKS</span></span>

[<span data-ttu-id="ddce9-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ddce9-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="ddce9-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ddce9-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)
