---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 78523d5bef3bfb2461bb524044da14f8aedbbc12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930117"
---
# <span data-ttu-id="fa31f-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fa31f-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="fa31f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa31f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa31f-103">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="fa31f-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa31f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa31f-104">SYNTAX</span></span>

### <span data-ttu-id="fa31f-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fa31f-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fa31f-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa31f-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fa31f-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa31f-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fa31f-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa31f-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fa31f-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa31f-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fa31f-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa31f-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="fa31f-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa31f-111">DESCRIPTION</span></span>
<span data-ttu-id="fa31f-112">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="fa31f-112">Filters active directory users.</span></span>

## <span data-ttu-id="fa31f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa31f-113">EXAMPLES</span></span>

### <span data-ttu-id="fa31f-114">Exempel 1 – Visa alla användare</span><span class="sxs-lookup"><span data-stu-id="fa31f-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="fa31f-115">Visar alla AD-användare i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="fa31f-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="fa31f-116">Exempel 2 – Visa alla användare som använder sid indelning</span><span class="sxs-lookup"><span data-stu-id="fa31f-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="fa31f-117">Visar de första 100 AD-användarna i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="fa31f-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="fa31f-118">Exempel 3 – få annons användare via användarens huvud namn</span><span class="sxs-lookup"><span data-stu-id="fa31f-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="fa31f-119">Får AD-användare med UPN " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="fa31f-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="fa31f-120">Exempel 4-lista efter Sök sträng</span><span class="sxs-lookup"><span data-stu-id="fa31f-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="fa31f-121">Visar alla AD-användare vars visnings namn börjar med "Johan".</span><span class="sxs-lookup"><span data-stu-id="fa31f-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="fa31f-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa31f-122">PARAMETERS</span></span>

### <span data-ttu-id="fa31f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa31f-123">-DefaultProfile</span></span>
<span data-ttu-id="fa31f-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fa31f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa31f-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fa31f-125">-DisplayName</span></span>
<span data-ttu-id="fa31f-126">Användarens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="fa31f-126">The display name of the user.</span></span>

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

### <span data-ttu-id="fa31f-127">-Först</span><span class="sxs-lookup"><span data-stu-id="fa31f-127">-First</span></span>
<span data-ttu-id="fa31f-128">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="fa31f-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="fa31f-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="fa31f-129">-IncludeTotalCount</span></span>
<span data-ttu-id="fa31f-130">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="fa31f-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="fa31f-131">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="fa31f-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="fa31f-132">-E-post</span><span class="sxs-lookup"><span data-stu-id="fa31f-132">-Mail</span></span>
<span data-ttu-id="fa31f-133">Användarens e-post.</span><span class="sxs-lookup"><span data-stu-id="fa31f-133">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa31f-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fa31f-134">-ObjectId</span></span>
<span data-ttu-id="fa31f-135">Användarens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="fa31f-135">Object id of the user.</span></span>

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

### <span data-ttu-id="fa31f-136">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="fa31f-136">-Skip</span></span>
<span data-ttu-id="fa31f-137">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="fa31f-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="fa31f-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="fa31f-138">-StartsWith</span></span>
<span data-ttu-id="fa31f-139">Används för att hitta användare som börjar med angiven sträng.</span><span class="sxs-lookup"><span data-stu-id="fa31f-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="fa31f-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fa31f-140">-UserPrincipalName</span></span>
<span data-ttu-id="fa31f-141">Användarens UPN.</span><span class="sxs-lookup"><span data-stu-id="fa31f-141">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa31f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa31f-142">CommonParameters</span></span>
<span data-ttu-id="fa31f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa31f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa31f-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa31f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa31f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa31f-145">INPUTS</span></span>

### <span data-ttu-id="fa31f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fa31f-146">System.String</span></span>

### <span data-ttu-id="fa31f-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="fa31f-147">System.Guid</span></span>

## <span data-ttu-id="fa31f-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa31f-148">OUTPUTS</span></span>

### <span data-ttu-id="fa31f-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="fa31f-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="fa31f-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa31f-150">NOTES</span></span>

## <span data-ttu-id="fa31f-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa31f-151">RELATED LINKS</span></span>

[<span data-ttu-id="fa31f-152">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fa31f-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)



[<span data-ttu-id="fa31f-153">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fa31f-153">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

