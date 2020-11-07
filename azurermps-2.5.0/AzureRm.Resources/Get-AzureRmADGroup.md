---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: 9ddc9658d6d18cc7a08df33f1f976521656c9234
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929630"
---
# <span data-ttu-id="6388d-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="6388d-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="6388d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6388d-102">SYNOPSIS</span></span>
<span data-ttu-id="6388d-103">Filtrerar Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="6388d-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6388d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6388d-104">SYNTAX</span></span>

### <span data-ttu-id="6388d-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6388d-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6388d-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6388d-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6388d-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6388d-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6388d-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6388d-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="6388d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6388d-109">DESCRIPTION</span></span>
<span data-ttu-id="6388d-110">Filtrerar Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="6388d-110">Filters active directory groups.</span></span>

## <span data-ttu-id="6388d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6388d-111">EXAMPLES</span></span>

### <span data-ttu-id="6388d-112">Exempel 1 – Visa alla AD-grupper</span><span class="sxs-lookup"><span data-stu-id="6388d-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="6388d-113">Visar alla AD-grupper i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="6388d-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="6388d-114">Exempel 2 – Visa alla AD-grupper med sid indelning</span><span class="sxs-lookup"><span data-stu-id="6388d-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="6388d-115">Visar de första 100 AD-grupperna i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="6388d-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="6388d-116">Exempel 3 – Hämta annons grupp efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="6388d-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="6388d-117">Hämtar en AD-grupp med objekt-ID ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="6388d-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="6388d-118">Exempel 4-lista grupper per Sök sträng</span><span class="sxs-lookup"><span data-stu-id="6388d-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="6388d-119">Visar alla AD-grupper vars visnings namn börjar med "Joe".</span><span class="sxs-lookup"><span data-stu-id="6388d-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="6388d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6388d-120">PARAMETERS</span></span>

### <span data-ttu-id="6388d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6388d-121">-DefaultProfile</span></span>
<span data-ttu-id="6388d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6388d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6388d-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6388d-123">-DisplayName</span></span>
<span data-ttu-id="6388d-124">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="6388d-124">The display name of the group.</span></span>

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

### <span data-ttu-id="6388d-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="6388d-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="6388d-126">Används för att hitta grupper som börjar med angiven sträng.</span><span class="sxs-lookup"><span data-stu-id="6388d-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="6388d-127">-Först</span><span class="sxs-lookup"><span data-stu-id="6388d-127">-First</span></span>
<span data-ttu-id="6388d-128">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="6388d-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="6388d-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="6388d-129">-IncludeTotalCount</span></span>
<span data-ttu-id="6388d-130">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6388d-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="6388d-131">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="6388d-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="6388d-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6388d-132">-ObjectId</span></span>
<span data-ttu-id="6388d-133">Objekt-ID för gruppen.</span><span class="sxs-lookup"><span data-stu-id="6388d-133">Object id of the group.</span></span>

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

### <span data-ttu-id="6388d-134">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="6388d-134">-Skip</span></span>
<span data-ttu-id="6388d-135">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="6388d-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="6388d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6388d-136">CommonParameters</span></span>
<span data-ttu-id="6388d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6388d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6388d-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6388d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6388d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6388d-139">INPUTS</span></span>

### <span data-ttu-id="6388d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6388d-140">System.String</span></span>

### <span data-ttu-id="6388d-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6388d-141">System.Guid</span></span>

## <span data-ttu-id="6388d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6388d-142">OUTPUTS</span></span>

### <span data-ttu-id="6388d-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="6388d-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="6388d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6388d-144">NOTES</span></span>

## <span data-ttu-id="6388d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6388d-145">RELATED LINKS</span></span>

[<span data-ttu-id="6388d-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6388d-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="6388d-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6388d-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="6388d-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="6388d-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

