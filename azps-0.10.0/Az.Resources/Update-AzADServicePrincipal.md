---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: e2c8e8fea9f8f86f06a9808158c50cb63915106b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923725"
---
# <span data-ttu-id="a9394-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a9394-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="a9394-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9394-102">SYNOPSIS</span></span>
<span data-ttu-id="a9394-103">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a9394-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="a9394-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9394-104">SYNTAX</span></span>

### <span data-ttu-id="a9394-105">SpObjectIdWithDisplayNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a9394-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9394-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9394-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9394-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9394-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9394-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9394-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9394-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9394-109">DESCRIPTION</span></span>
<span data-ttu-id="a9394-110">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a9394-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="a9394-111">Använd New-AzADSpCredential cmdlet för att uppdatera autentiseringsuppgifterna som är associerade med den här tjänstens huvud säkerhets objekt.</span><span class="sxs-lookup"><span data-stu-id="a9394-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="a9394-112">Använd Update-AzADApplication cmdlet för att uppdatera egenskaperna för det underliggande programmet.</span><span class="sxs-lookup"><span data-stu-id="a9394-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="a9394-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9394-113">EXAMPLES</span></span>

### <span data-ttu-id="a9394-114">Exempel 1 – uppdatera visnings namnet för ett tjänst huvud konto</span><span class="sxs-lookup"><span data-stu-id="a9394-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="a9394-115">Uppdaterar visnings namnet för tjänstens huvud namn med objekt-ID ' 784136ca-3ae2-4fdd-a388-89d793e7c780 ' som ska vara ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="a9394-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="a9394-116">Exempel 2 – uppdatera visnings namnet för ett tjänst huvud med rör</span><span class="sxs-lookup"><span data-stu-id="a9394-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="a9394-117">Hämtar tjänstens huvud namn med objekt-ID ' 784136ca-3ae2-4fdd-a388-89d793e7c780 ' och pipes till Update-AzADServicePrincipal cmdlet för att uppdatera visnings namnet för tjänstens huvud konto till "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="a9394-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="a9394-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9394-118">PARAMETERS</span></span>

### <span data-ttu-id="a9394-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a9394-119">-ApplicationId</span></span>
<span data-ttu-id="a9394-120">Program-ID för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="a9394-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="a9394-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9394-121">-DefaultProfile</span></span>
<span data-ttu-id="a9394-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9394-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9394-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a9394-123">-DisplayName</span></span>
<span data-ttu-id="a9394-124">Visnings namnet för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="a9394-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="a9394-125">-Start Sidan</span><span class="sxs-lookup"><span data-stu-id="a9394-125">-Homepage</span></span>
<span data-ttu-id="a9394-126">Start sidan för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="a9394-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="a9394-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="a9394-127">-IdentifierUri</span></span>
<span data-ttu-id="a9394-128">Identitets-URI för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="a9394-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="a9394-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9394-129">-InputObject</span></span>
<span data-ttu-id="a9394-130">Det objekt som representerar tjänstens huvud konto att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="a9394-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9394-131">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="a9394-131">-KeyCredential</span></span>
<span data-ttu-id="a9394-132">De viktigaste autentiseringsuppgifterna för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="a9394-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9394-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a9394-133">-ObjectId</span></span>
<span data-ttu-id="a9394-134">Objekt-ID för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="a9394-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9394-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="a9394-135">-PasswordCredential</span></span>
<span data-ttu-id="a9394-136">Autentiseringsuppgifterna för lösen ordet för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="a9394-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9394-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a9394-137">-ServicePrincipalName</span></span>
<span data-ttu-id="a9394-138">SPN för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="a9394-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="a9394-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9394-139">-Confirm</span></span>
<span data-ttu-id="a9394-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9394-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9394-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9394-141">-WhatIf</span></span>
<span data-ttu-id="a9394-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9394-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9394-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9394-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9394-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9394-144">CommonParameters</span></span>
<span data-ttu-id="a9394-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9394-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9394-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9394-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9394-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9394-147">INPUTS</span></span>

### <span data-ttu-id="a9394-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a9394-148">System.Guid</span></span>

### <span data-ttu-id="a9394-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a9394-149">System.String</span></span>

### <span data-ttu-id="a9394-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a9394-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="a9394-151">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a9394-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a9394-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9394-152">OUTPUTS</span></span>

### <span data-ttu-id="a9394-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a9394-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="a9394-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9394-154">NOTES</span></span>

## <span data-ttu-id="a9394-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9394-155">RELATED LINKS</span></span>
