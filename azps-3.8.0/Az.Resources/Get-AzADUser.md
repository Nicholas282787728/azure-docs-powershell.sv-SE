---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: d0391b47e4060b2b93206c8e4d2722ca682a0db4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927370"
---
# <span data-ttu-id="d14bc-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d14bc-101">Get-AzADUser</span></span>

## <span data-ttu-id="d14bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d14bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d14bc-103">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="d14bc-103">Filters active directory users.</span></span>

## <span data-ttu-id="d14bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d14bc-104">SYNTAX</span></span>

### <span data-ttu-id="d14bc-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d14bc-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d14bc-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d14bc-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d14bc-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d14bc-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d14bc-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d14bc-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d14bc-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d14bc-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d14bc-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="d14bc-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="d14bc-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d14bc-111">DESCRIPTION</span></span>
<span data-ttu-id="d14bc-112">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="d14bc-112">Filters active directory users.</span></span>

## <span data-ttu-id="d14bc-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d14bc-113">EXAMPLES</span></span>

### <span data-ttu-id="d14bc-114">Exempel 1 – Visa alla användare</span><span class="sxs-lookup"><span data-stu-id="d14bc-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="d14bc-115">Visar alla AD-användare i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="d14bc-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="d14bc-116">Exempel 2 – Visa alla användare som använder sid indelning</span><span class="sxs-lookup"><span data-stu-id="d14bc-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="d14bc-117">Visar de första 100 AD-användarna i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="d14bc-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="d14bc-118">Exempel 3 – få annons användare via användarens huvud namn</span><span class="sxs-lookup"><span data-stu-id="d14bc-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="d14bc-119">Får AD-användare med UPN " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="d14bc-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="d14bc-120">Exempel 4-lista efter Sök sträng</span><span class="sxs-lookup"><span data-stu-id="d14bc-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="d14bc-121">Visar alla AD-användare vars visnings namn börjar med "Johan".</span><span class="sxs-lookup"><span data-stu-id="d14bc-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="d14bc-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d14bc-122">PARAMETERS</span></span>

### <span data-ttu-id="d14bc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14bc-123">-DefaultProfile</span></span>
<span data-ttu-id="d14bc-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d14bc-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d14bc-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d14bc-125">-DisplayName</span></span>
<span data-ttu-id="d14bc-126">Användarens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="d14bc-126">The display name of the user.</span></span>

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

### <span data-ttu-id="d14bc-127">-E-post</span><span class="sxs-lookup"><span data-stu-id="d14bc-127">-Mail</span></span>
<span data-ttu-id="d14bc-128">Användarens e-post.</span><span class="sxs-lookup"><span data-stu-id="d14bc-128">The user mail.</span></span>

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

### <span data-ttu-id="d14bc-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d14bc-129">-ObjectId</span></span>
<span data-ttu-id="d14bc-130">Användarens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="d14bc-130">Object id of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d14bc-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="d14bc-131">-StartsWith</span></span>
<span data-ttu-id="d14bc-132">Används för att hitta användare som börjar med angiven sträng.</span><span class="sxs-lookup"><span data-stu-id="d14bc-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="d14bc-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d14bc-133">-UserPrincipalName</span></span>
<span data-ttu-id="d14bc-134">Användarens UPN.</span><span class="sxs-lookup"><span data-stu-id="d14bc-134">UPN of the user.</span></span>

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

### <span data-ttu-id="d14bc-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="d14bc-135">-IncludeTotalCount</span></span>
<span data-ttu-id="d14bc-136">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d14bc-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="d14bc-137">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="d14bc-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="d14bc-138">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="d14bc-138">-Skip</span></span>
<span data-ttu-id="d14bc-139">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="d14bc-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="d14bc-140">-Först</span><span class="sxs-lookup"><span data-stu-id="d14bc-140">-First</span></span>
<span data-ttu-id="d14bc-141">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="d14bc-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="d14bc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14bc-142">CommonParameters</span></span>
<span data-ttu-id="d14bc-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d14bc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d14bc-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d14bc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14bc-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d14bc-145">INPUTS</span></span>

### <span data-ttu-id="d14bc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d14bc-146">System.String</span></span>

## <span data-ttu-id="d14bc-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d14bc-147">OUTPUTS</span></span>

### <span data-ttu-id="d14bc-148">Microsoft. Azure. commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="d14bc-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="d14bc-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d14bc-149">NOTES</span></span>

## <span data-ttu-id="d14bc-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d14bc-150">RELATED LINKS</span></span>

[<span data-ttu-id="d14bc-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d14bc-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="d14bc-152">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d14bc-152">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="d14bc-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d14bc-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

