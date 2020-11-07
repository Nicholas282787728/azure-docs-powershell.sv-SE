---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 34a00ed29d40d8824ac0f2d24f5275bb7c0a0164
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924049"
---
# <span data-ttu-id="86ab4-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86ab4-101">Get-AzADUser</span></span>

## <span data-ttu-id="86ab4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="86ab4-103">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="86ab4-103">Filters active directory users.</span></span>

## <span data-ttu-id="86ab4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86ab4-104">SYNTAX</span></span>

### <span data-ttu-id="86ab4-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="86ab4-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="86ab4-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="86ab4-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="86ab4-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86ab4-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="86ab4-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86ab4-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="86ab4-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="86ab4-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="86ab4-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="86ab4-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="86ab4-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86ab4-111">DESCRIPTION</span></span>
<span data-ttu-id="86ab4-112">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="86ab4-112">Filters active directory users.</span></span>

## <span data-ttu-id="86ab4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86ab4-113">EXAMPLES</span></span>

### <span data-ttu-id="86ab4-114">Exempel 1 – Visa alla användare</span><span class="sxs-lookup"><span data-stu-id="86ab4-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="86ab4-115">Visar alla AD-användare i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="86ab4-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="86ab4-116">Exempel 2 – Visa alla användare som använder sid indelning</span><span class="sxs-lookup"><span data-stu-id="86ab4-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="86ab4-117">Visar de första 100 AD-användarna i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="86ab4-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="86ab4-118">Exempel 3 – få annons användare via användarens huvud namn</span><span class="sxs-lookup"><span data-stu-id="86ab4-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="86ab4-119">Får AD-användare med UPN " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="86ab4-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="86ab4-120">Exempel 4-lista efter Sök sträng</span><span class="sxs-lookup"><span data-stu-id="86ab4-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="86ab4-121">Visar alla AD-användare vars visnings namn börjar med "Johan".</span><span class="sxs-lookup"><span data-stu-id="86ab4-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="86ab4-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86ab4-122">PARAMETERS</span></span>

### <span data-ttu-id="86ab4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ab4-123">-DefaultProfile</span></span>
<span data-ttu-id="86ab4-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="86ab4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86ab4-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="86ab4-125">-DisplayName</span></span>
<span data-ttu-id="86ab4-126">Användarens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="86ab4-126">The display name of the user.</span></span>

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

### <span data-ttu-id="86ab4-127">-Först</span><span class="sxs-lookup"><span data-stu-id="86ab4-127">-First</span></span>
<span data-ttu-id="86ab4-128">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="86ab4-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="86ab4-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="86ab4-129">-IncludeTotalCount</span></span>
<span data-ttu-id="86ab4-130">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="86ab4-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="86ab4-131">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="86ab4-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="86ab4-132">-E-post</span><span class="sxs-lookup"><span data-stu-id="86ab4-132">-Mail</span></span>
<span data-ttu-id="86ab4-133">Användarens e-post.</span><span class="sxs-lookup"><span data-stu-id="86ab4-133">The user mail.</span></span>

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

### <span data-ttu-id="86ab4-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="86ab4-134">-ObjectId</span></span>
<span data-ttu-id="86ab4-135">Användarens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="86ab4-135">Object id of the user.</span></span>

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

### <span data-ttu-id="86ab4-136">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="86ab4-136">-Skip</span></span>
<span data-ttu-id="86ab4-137">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="86ab4-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="86ab4-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="86ab4-138">-StartsWith</span></span>
<span data-ttu-id="86ab4-139">Används för att hitta användare som börjar med angiven sträng.</span><span class="sxs-lookup"><span data-stu-id="86ab4-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="86ab4-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="86ab4-140">-UserPrincipalName</span></span>
<span data-ttu-id="86ab4-141">Användarens UPN.</span><span class="sxs-lookup"><span data-stu-id="86ab4-141">UPN of the user.</span></span>

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

### <span data-ttu-id="86ab4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ab4-142">CommonParameters</span></span>
<span data-ttu-id="86ab4-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ab4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ab4-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ab4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ab4-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86ab4-145">INPUTS</span></span>

### <span data-ttu-id="86ab4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="86ab4-146">System.String</span></span>

### <span data-ttu-id="86ab4-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="86ab4-147">System.Guid</span></span>

## <span data-ttu-id="86ab4-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86ab4-148">OUTPUTS</span></span>

### <span data-ttu-id="86ab4-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="86ab4-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="86ab4-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86ab4-150">NOTES</span></span>

## <span data-ttu-id="86ab4-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86ab4-151">RELATED LINKS</span></span>

[<span data-ttu-id="86ab4-152">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86ab4-152">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="86ab4-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86ab4-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="86ab4-154">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86ab4-154">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

