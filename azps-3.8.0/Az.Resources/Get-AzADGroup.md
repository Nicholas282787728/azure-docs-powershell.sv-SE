---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 32370d88de54b7a6004da6b66e15e08c9eca26e7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089754"
---
# <span data-ttu-id="b5334-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="b5334-101">Get-AzADGroup</span></span>

## <span data-ttu-id="b5334-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5334-102">SYNOPSIS</span></span>
<span data-ttu-id="b5334-103">Filtrerar Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="b5334-103">Filters active directory groups.</span></span>

## <span data-ttu-id="b5334-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5334-104">SYNTAX</span></span>

### <span data-ttu-id="b5334-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b5334-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b5334-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5334-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b5334-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5334-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b5334-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5334-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="b5334-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5334-109">DESCRIPTION</span></span>
<span data-ttu-id="b5334-110">Filtrerar Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="b5334-110">Filters active directory groups.</span></span>

## <span data-ttu-id="b5334-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5334-111">EXAMPLES</span></span>

### <span data-ttu-id="b5334-112">Exempel 1 – Visa alla AD-grupper</span><span class="sxs-lookup"><span data-stu-id="b5334-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzADGroup
```

<span data-ttu-id="b5334-113">Visar alla AD-grupper i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="b5334-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="b5334-114">Exempel 2 – Visa alla AD-grupper med sid indelning</span><span class="sxs-lookup"><span data-stu-id="b5334-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="b5334-115">Visar de första 100 AD-grupperna i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="b5334-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="b5334-116">Exempel 3 – Hämta annons grupp efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="b5334-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="b5334-117">Hämtar en AD-grupp med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="b5334-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="b5334-118">Exempel 4-lista grupper per Sök sträng</span><span class="sxs-lookup"><span data-stu-id="b5334-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="b5334-119">Visar alla AD-grupper vars visnings namn börjar med "Joe".</span><span class="sxs-lookup"><span data-stu-id="b5334-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="b5334-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5334-120">PARAMETERS</span></span>

### <span data-ttu-id="b5334-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5334-121">-DefaultProfile</span></span>
<span data-ttu-id="b5334-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b5334-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5334-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b5334-123">-DisplayName</span></span>
<span data-ttu-id="b5334-124">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="b5334-124">The display name of the group.</span></span>

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

### <span data-ttu-id="b5334-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="b5334-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="b5334-126">Används för att hitta grupper som börjar med angiven sträng.</span><span class="sxs-lookup"><span data-stu-id="b5334-126">Used to find groups that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5334-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b5334-127">-ObjectId</span></span>
<span data-ttu-id="b5334-128">Objekt-ID för gruppen.</span><span class="sxs-lookup"><span data-stu-id="b5334-128">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="b5334-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="b5334-129">-IncludeTotalCount</span></span>
<span data-ttu-id="b5334-130">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="b5334-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="b5334-131">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="b5334-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="b5334-132">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="b5334-132">-Skip</span></span>
<span data-ttu-id="b5334-133">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="b5334-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="b5334-134">-Först</span><span class="sxs-lookup"><span data-stu-id="b5334-134">-First</span></span>
<span data-ttu-id="b5334-135">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="b5334-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="b5334-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5334-136">CommonParameters</span></span>
<span data-ttu-id="b5334-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5334-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5334-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5334-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5334-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5334-139">INPUTS</span></span>

### <span data-ttu-id="b5334-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b5334-140">System.String</span></span>

### <span data-ttu-id="b5334-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b5334-141">System.Guid</span></span>

## <span data-ttu-id="b5334-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5334-142">OUTPUTS</span></span>

### <span data-ttu-id="b5334-143">Microsoft. Azure. commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="b5334-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="b5334-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5334-144">NOTES</span></span>

## <span data-ttu-id="b5334-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5334-145">RELATED LINKS</span></span>

[<span data-ttu-id="b5334-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="b5334-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="b5334-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b5334-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="b5334-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="b5334-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)
