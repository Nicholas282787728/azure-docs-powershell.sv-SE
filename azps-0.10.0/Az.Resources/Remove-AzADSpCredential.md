---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: 39796e1e9d77fb95c65b7ac72e9dee3ee266af10
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923857"
---
# <span data-ttu-id="031af-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="031af-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="031af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="031af-102">SYNOPSIS</span></span>
<span data-ttu-id="031af-103">Tar bort en autentiseringsuppgift från ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="031af-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="031af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="031af-104">SYNTAX</span></span>

### <span data-ttu-id="031af-105">ObjectIdWithKeyIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="031af-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="031af-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="031af-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="031af-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="031af-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="031af-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="031af-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="031af-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="031af-109">DESCRIPTION</span></span>
<span data-ttu-id="031af-110">Du kan använda Remove-AzADSpCredential cmdlet för att ta bort en behörighets nycklar från ett säkerhets objekt om det rör sig om en kompromiss eller en del av förnyelsen av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="031af-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="031af-111">Tjänstens huvud namn identifieras genom att ange antingen objekt-ID eller SPN (Service Principal Name).</span><span class="sxs-lookup"><span data-stu-id="031af-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="031af-112">Den autentiseringsuppgift som ska tas bort identifieras via dess tillhör ande ID om en enskild autentiseringsuppgift ska tas bort eller med en "alla"-växel för att ta bort alla autentiseringsuppgifter som är kopplade till tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="031af-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="031af-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="031af-113">EXAMPLES</span></span>

### <span data-ttu-id="031af-114">Exempel 1 – ta bort en specifik autentiseringsuppgift från ett SPN-namn</span><span class="sxs-lookup"><span data-stu-id="031af-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="031af-115">Tar bort autentiseringsuppgiften med ID ' 9044423a-60a3-45ac-9ab1-09534157ebb ' från tjänstens huvud namn med objekt-ID ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 '.</span><span class="sxs-lookup"><span data-stu-id="031af-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="031af-116">Exempel 2 – ta bort alla autentiseringsuppgifter från ett huvud säkerhets objekt</span><span class="sxs-lookup"><span data-stu-id="031af-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="031af-117">Tar bort alla autentiseringsuppgifter från tjänstens huvud konto med SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="031af-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="031af-118">Exempel 3 – ta bort alla autentiseringsuppgifter från ett tjänst huvud med ledning</span><span class="sxs-lookup"><span data-stu-id="031af-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="031af-119">Hämtar tjänstens huvud namn med objekt-ID ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' och pipes till Remove-AzADSpCredential cmdlet för att ta bort alla autentiseringsuppgifter från den tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="031af-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="031af-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="031af-120">PARAMETERS</span></span>

### <span data-ttu-id="031af-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="031af-121">-DefaultProfile</span></span>
<span data-ttu-id="031af-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="031af-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="031af-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="031af-123">-DisplayName</span></span>
<span data-ttu-id="031af-124">Visnings namnet på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="031af-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031af-125">-Force</span><span class="sxs-lookup"><span data-stu-id="031af-125">-Force</span></span>
<span data-ttu-id="031af-126">Växla till att ta bort autentiseringsuppgiften utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="031af-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="031af-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="031af-127">-KeyId</span></span>
<span data-ttu-id="031af-128">Anger den autentiseringsinformation som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="031af-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="031af-129">Huvud-ID: na för ett tjänst huvud konto kan erhållas med hjälp av Get-AzADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="031af-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031af-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="031af-130">-ObjectId</span></span>
<span data-ttu-id="031af-131">Objekt-ID för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="031af-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031af-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="031af-132">-PassThru</span></span>
<span data-ttu-id="031af-133">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="031af-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="031af-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="031af-134">-ServicePrincipalName</span></span>
<span data-ttu-id="031af-135">Namnet (SPN) för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="031af-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031af-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="031af-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="031af-137">Tjänst huvud objekt som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="031af-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="031af-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="031af-138">-Confirm</span></span>
<span data-ttu-id="031af-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="031af-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="031af-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="031af-140">-WhatIf</span></span>
<span data-ttu-id="031af-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="031af-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="031af-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="031af-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="031af-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="031af-143">CommonParameters</span></span>
<span data-ttu-id="031af-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="031af-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="031af-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="031af-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="031af-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="031af-146">INPUTS</span></span>

### <span data-ttu-id="031af-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="031af-147">System.Guid</span></span>

### <span data-ttu-id="031af-148">System. String</span><span class="sxs-lookup"><span data-stu-id="031af-148">System.String</span></span>

### <span data-ttu-id="031af-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="031af-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="031af-150">Parametrar: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="031af-150">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="031af-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="031af-151">OUTPUTS</span></span>

### <span data-ttu-id="031af-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="031af-152">System.Boolean</span></span>

## <span data-ttu-id="031af-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="031af-153">NOTES</span></span>

## <span data-ttu-id="031af-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="031af-154">RELATED LINKS</span></span>

[<span data-ttu-id="031af-155">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="031af-155">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="031af-156">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="031af-156">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="031af-157">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="031af-157">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

