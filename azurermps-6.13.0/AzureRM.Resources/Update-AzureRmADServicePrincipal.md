---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADServicePrincipal.md
ms.openlocfilehash: ce778da76b0dfc81a8438bdd0fdc3e0a20215843
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585855"
---
# <span data-ttu-id="2bac0-101">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2bac0-101">Update-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="2bac0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bac0-102">SYNOPSIS</span></span>
<span data-ttu-id="2bac0-103">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2bac0-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bac0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bac0-104">SYNTAX</span></span>

### <span data-ttu-id="2bac0-105">SpObjectIdWithDisplayNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2bac0-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzureRmADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bac0-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bac0-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bac0-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bac0-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bac0-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bac0-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2bac0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bac0-109">DESCRIPTION</span></span>
<span data-ttu-id="2bac0-110">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2bac0-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="2bac0-111">Använd New-AzureRmADSpCredential cmdlet för att uppdatera autentiseringsuppgifterna som är associerade med den här tjänstens huvud säkerhets objekt.</span><span class="sxs-lookup"><span data-stu-id="2bac0-111">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="2bac0-112">Använd Update-AzureRmADApplication cmdlet för att uppdatera egenskaperna för det underliggande programmet.</span><span class="sxs-lookup"><span data-stu-id="2bac0-112">To update the properties associated with the underlying application, please use Update-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="2bac0-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bac0-113">EXAMPLES</span></span>

### <span data-ttu-id="2bac0-114">Exempel 1 – uppdatera visnings namnet för ett tjänst huvud konto</span><span class="sxs-lookup"><span data-stu-id="2bac0-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="2bac0-115">Uppdaterar visnings namnet för tjänstens huvud namn med objekt-ID ' 784136ca-3ae2-4fdd-a388-89d793e7c780 ' som ska vara ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="2bac0-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="2bac0-116">Exempel 2 – uppdatera visnings namnet för ett tjänst huvud med rör</span><span class="sxs-lookup"><span data-stu-id="2bac0-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzureRmADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="2bac0-117">Hämtar tjänstens huvud namn med objekt-ID ' 784136ca-3ae2-4fdd-a388-89d793e7c780 ' och pipes till Update-AzureRmADServicePrincipal cmdlet för att uppdatera visnings namnet för tjänstens huvud konto till "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="2bac0-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzureRmADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="2bac0-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bac0-118">PARAMETERS</span></span>

### <span data-ttu-id="2bac0-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2bac0-119">-ApplicationId</span></span>
<span data-ttu-id="2bac0-120">Program-ID för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="2bac0-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="2bac0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bac0-121">-DefaultProfile</span></span>
<span data-ttu-id="2bac0-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bac0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bac0-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2bac0-123">-DisplayName</span></span>
<span data-ttu-id="2bac0-124">Visnings namnet för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="2bac0-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="2bac0-125">-Start Sidan</span><span class="sxs-lookup"><span data-stu-id="2bac0-125">-Homepage</span></span>
<span data-ttu-id="2bac0-126">Start sidan för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="2bac0-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="2bac0-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="2bac0-127">-IdentifierUri</span></span>
<span data-ttu-id="2bac0-128">Identitets-URI för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="2bac0-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="2bac0-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bac0-129">-InputObject</span></span>
<span data-ttu-id="2bac0-130">Det objekt som representerar tjänstens huvud konto att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="2bac0-130">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="2bac0-131">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="2bac0-131">-KeyCredential</span></span>
<span data-ttu-id="2bac0-132">De viktigaste autentiseringsuppgifterna för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="2bac0-132">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="2bac0-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2bac0-133">-ObjectId</span></span>
<span data-ttu-id="2bac0-134">Objekt-ID för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="2bac0-134">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="2bac0-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="2bac0-135">-PasswordCredential</span></span>
<span data-ttu-id="2bac0-136">Autentiseringsuppgifterna för lösen ordet för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="2bac0-136">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="2bac0-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2bac0-137">-ServicePrincipalName</span></span>
<span data-ttu-id="2bac0-138">SPN för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="2bac0-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="2bac0-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2bac0-139">-Confirm</span></span>
<span data-ttu-id="2bac0-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2bac0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bac0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bac0-141">-WhatIf</span></span>
<span data-ttu-id="2bac0-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2bac0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bac0-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2bac0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bac0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bac0-144">CommonParameters</span></span>
<span data-ttu-id="2bac0-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bac0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bac0-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bac0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bac0-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bac0-147">INPUTS</span></span>

### <span data-ttu-id="2bac0-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2bac0-148">System.Guid</span></span>

### <span data-ttu-id="2bac0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2bac0-149">System.String</span></span>

### <span data-ttu-id="2bac0-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2bac0-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="2bac0-151">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2bac0-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2bac0-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bac0-152">OUTPUTS</span></span>

### <span data-ttu-id="2bac0-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2bac0-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="2bac0-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bac0-154">NOTES</span></span>

## <span data-ttu-id="2bac0-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bac0-155">RELATED LINKS</span></span>
