---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 05bd5f7997c83c2be6b50faf0e6d88ee7413a773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324276"
---
# <span data-ttu-id="86c1c-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="86c1c-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="86c1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="86c1c-103">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="86c1c-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="86c1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86c1c-104">SYNTAX</span></span>

### <span data-ttu-id="86c1c-105">SpObjectIdWithDisplayNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="86c1c-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c1c-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c1c-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c1c-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c1c-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c1c-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c1c-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c1c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86c1c-109">DESCRIPTION</span></span>
<span data-ttu-id="86c1c-110">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="86c1c-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="86c1c-111">Använd New-AzADSpCredential cmdlet för att uppdatera autentiseringsuppgifterna som är associerade med den här tjänstens huvud säkerhets objekt.</span><span class="sxs-lookup"><span data-stu-id="86c1c-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="86c1c-112">Använd Update-AzADApplication cmdlet för att uppdatera egenskaperna för det underliggande programmet.</span><span class="sxs-lookup"><span data-stu-id="86c1c-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="86c1c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86c1c-113">EXAMPLES</span></span>

### <span data-ttu-id="86c1c-114">Exempel 1: uppdatera visnings namnet för ett tjänst huvud konto</span><span class="sxs-lookup"><span data-stu-id="86c1c-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="86c1c-115">Uppdaterar visnings namnet för tjänstens huvud namn med objekt-ID ' 784136ca-3ae2-4fdd-a388-89d793e7c780 ' som ska vara ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="86c1c-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="86c1c-116">Exempel 2: uppdatera visnings namnet för ett tjänst huvud med rör</span><span class="sxs-lookup"><span data-stu-id="86c1c-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="86c1c-117">Hämtar tjänstens huvud namn med objekt-ID ' 784136ca-3ae2-4fdd-a388-89d793e7c780 ' och pipes till Update-AzADServicePrincipal cmdlet för att uppdatera visnings namnet för tjänstens huvud konto till "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="86c1c-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="86c1c-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="86c1c-118">Example 3</span></span>

<span data-ttu-id="86c1c-119">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="86c1c-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="86c1c-120">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="86c1c-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="86c1c-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86c1c-121">PARAMETERS</span></span>

### <span data-ttu-id="86c1c-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="86c1c-122">-ApplicationId</span></span>
<span data-ttu-id="86c1c-123">Program-ID för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="86c1c-123">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c1c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c1c-124">-DefaultProfile</span></span>
<span data-ttu-id="86c1c-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86c1c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86c1c-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="86c1c-126">-DisplayName</span></span>
<span data-ttu-id="86c1c-127">Visnings namnet för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="86c1c-127">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c1c-128">-Start Sidan</span><span class="sxs-lookup"><span data-stu-id="86c1c-128">-Homepage</span></span>
<span data-ttu-id="86c1c-129">Start sidan för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="86c1c-129">The homepage for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c1c-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="86c1c-130">-IdentifierUri</span></span>
<span data-ttu-id="86c1c-131">Identitets-URI för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="86c1c-131">The identifier URI(s) for the service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c1c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86c1c-132">-InputObject</span></span>
<span data-ttu-id="86c1c-133">Det objekt som representerar tjänstens huvud konto att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="86c1c-133">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86c1c-134">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="86c1c-134">-KeyCredential</span></span>
<span data-ttu-id="86c1c-135">De viktigaste autentiseringsuppgifterna för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="86c1c-135">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c1c-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="86c1c-136">-ObjectId</span></span>
<span data-ttu-id="86c1c-137">Objekt-ID för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="86c1c-137">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c1c-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="86c1c-138">-PasswordCredential</span></span>
<span data-ttu-id="86c1c-139">Autentiseringsuppgifterna för lösen ordet för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="86c1c-139">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c1c-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="86c1c-140">-ServicePrincipalName</span></span>
<span data-ttu-id="86c1c-141">SPN för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="86c1c-141">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c1c-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86c1c-142">-Confirm</span></span>
<span data-ttu-id="86c1c-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86c1c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c1c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c1c-144">-WhatIf</span></span>
<span data-ttu-id="86c1c-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86c1c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c1c-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86c1c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c1c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c1c-147">CommonParameters</span></span>
<span data-ttu-id="86c1c-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c1c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c1c-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86c1c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c1c-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86c1c-150">INPUTS</span></span>

### <span data-ttu-id="86c1c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="86c1c-151">System.String</span></span>

### <span data-ttu-id="86c1c-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="86c1c-152">System.Guid</span></span>

### <span data-ttu-id="86c1c-153">Microsoft. Azure. commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="86c1c-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="86c1c-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86c1c-154">OUTPUTS</span></span>

### <span data-ttu-id="86c1c-155">Microsoft. Azure. commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="86c1c-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="86c1c-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86c1c-156">NOTES</span></span>

## <span data-ttu-id="86c1c-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86c1c-157">RELATED LINKS</span></span>