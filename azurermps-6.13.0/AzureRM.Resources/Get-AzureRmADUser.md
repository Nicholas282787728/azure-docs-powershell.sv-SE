---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: b19571025aeb6349277e9ae366146774862e8a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755815"
---
# <span data-ttu-id="a6530-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a6530-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="a6530-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6530-102">SYNOPSIS</span></span>
<span data-ttu-id="a6530-103">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="a6530-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6530-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6530-104">SYNTAX</span></span>

### <span data-ttu-id="a6530-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a6530-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a6530-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6530-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a6530-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6530-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a6530-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6530-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a6530-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6530-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a6530-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6530-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="a6530-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6530-111">DESCRIPTION</span></span>
<span data-ttu-id="a6530-112">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="a6530-112">Filters active directory users.</span></span>

## <span data-ttu-id="a6530-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6530-113">EXAMPLES</span></span>

### <span data-ttu-id="a6530-114">Exempel 1 – Visa alla användare</span><span class="sxs-lookup"><span data-stu-id="a6530-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="a6530-115">Visar alla AD-användare i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="a6530-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="a6530-116">Exempel 2 – Visa alla användare som använder sid indelning</span><span class="sxs-lookup"><span data-stu-id="a6530-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="a6530-117">Visar de första 100 AD-användarna i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="a6530-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="a6530-118">Exempel 3 – få annons användare via användarens huvud namn</span><span class="sxs-lookup"><span data-stu-id="a6530-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="a6530-119">Får AD-användare med UPN " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="a6530-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="a6530-120">Exempel 4-lista efter Sök sträng</span><span class="sxs-lookup"><span data-stu-id="a6530-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="a6530-121">Visar alla AD-användare vars visnings namn börjar med "Johan".</span><span class="sxs-lookup"><span data-stu-id="a6530-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="a6530-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6530-122">PARAMETERS</span></span>

### <span data-ttu-id="a6530-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6530-123">-DefaultProfile</span></span>
<span data-ttu-id="a6530-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a6530-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6530-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a6530-125">-DisplayName</span></span>
<span data-ttu-id="a6530-126">Användarens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="a6530-126">The display name of the user.</span></span>

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

### <span data-ttu-id="a6530-127">-Först</span><span class="sxs-lookup"><span data-stu-id="a6530-127">-First</span></span>
<span data-ttu-id="a6530-128">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="a6530-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="a6530-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="a6530-129">-IncludeTotalCount</span></span>
<span data-ttu-id="a6530-130">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="a6530-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="a6530-131">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="a6530-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="a6530-132">-E-post</span><span class="sxs-lookup"><span data-stu-id="a6530-132">-Mail</span></span>
<span data-ttu-id="a6530-133">Användarens e-post.</span><span class="sxs-lookup"><span data-stu-id="a6530-133">The user mail.</span></span>

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

### <span data-ttu-id="a6530-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a6530-134">-ObjectId</span></span>
<span data-ttu-id="a6530-135">Användarens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="a6530-135">Object id of the user.</span></span>

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

### <span data-ttu-id="a6530-136">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="a6530-136">-Skip</span></span>
<span data-ttu-id="a6530-137">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="a6530-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="a6530-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="a6530-138">-StartsWith</span></span>
<span data-ttu-id="a6530-139">Används för att hitta användare som börjar med angiven sträng.</span><span class="sxs-lookup"><span data-stu-id="a6530-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="a6530-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a6530-140">-UserPrincipalName</span></span>
<span data-ttu-id="a6530-141">Användarens UPN.</span><span class="sxs-lookup"><span data-stu-id="a6530-141">UPN of the user.</span></span>

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

### <span data-ttu-id="a6530-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6530-142">CommonParameters</span></span>
<span data-ttu-id="a6530-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6530-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6530-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6530-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6530-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6530-145">INPUTS</span></span>

### <span data-ttu-id="a6530-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a6530-146">System.String</span></span>

### <span data-ttu-id="a6530-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a6530-147">System.Guid</span></span>

## <span data-ttu-id="a6530-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6530-148">OUTPUTS</span></span>

### <span data-ttu-id="a6530-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="a6530-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="a6530-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6530-150">NOTES</span></span>

## <span data-ttu-id="a6530-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6530-151">RELATED LINKS</span></span>

[<span data-ttu-id="a6530-152">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a6530-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="a6530-153">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a6530-153">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="a6530-154">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a6530-154">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

