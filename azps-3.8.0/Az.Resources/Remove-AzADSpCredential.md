---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: 669a1beecaed14c0ab0705979188995daaf9d95f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926429"
---
# <span data-ttu-id="a8eba-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a8eba-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="a8eba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8eba-102">SYNOPSIS</span></span>
<span data-ttu-id="a8eba-103">Tar bort en autentiseringsuppgift från ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="a8eba-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="a8eba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8eba-104">SYNTAX</span></span>

### <span data-ttu-id="a8eba-105">ObjectIdWithKeyIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a8eba-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8eba-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8eba-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8eba-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8eba-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8eba-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8eba-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8eba-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8eba-109">DESCRIPTION</span></span>
<span data-ttu-id="a8eba-110">Du kan använda Remove-AzADSpCredential cmdlet för att ta bort en behörighets nycklar från ett säkerhets objekt om det rör sig om en kompromiss eller en del av förnyelsen av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="a8eba-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="a8eba-111">Tjänstens huvud namn identifieras genom att ange antingen objekt-ID eller SPN (Service Principal Name).</span><span class="sxs-lookup"><span data-stu-id="a8eba-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="a8eba-112">Den autentiseringsuppgift som ska tas bort identifieras via dess tillhör ande ID om en enskild autentiseringsuppgift ska tas bort eller med en "alla"-växel för att ta bort alla autentiseringsuppgifter som är kopplade till tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="a8eba-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="a8eba-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8eba-113">EXAMPLES</span></span>

### <span data-ttu-id="a8eba-114">Exempel 1 – ta bort en specifik autentiseringsuppgift från ett SPN-namn</span><span class="sxs-lookup"><span data-stu-id="a8eba-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="a8eba-115">Tar bort autentiseringsuppgiften med ID ' 9044423a-60a3-45ac-9ab1-09534157ebb ' från tjänstens huvud namn med objekt-ID ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 '.</span><span class="sxs-lookup"><span data-stu-id="a8eba-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="a8eba-116">Exempel 2 – ta bort alla autentiseringsuppgifter från ett huvud säkerhets objekt</span><span class="sxs-lookup"><span data-stu-id="a8eba-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="a8eba-117">Tar bort alla autentiseringsuppgifter från tjänstens huvud konto med SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="a8eba-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="a8eba-118">Exempel 3 – ta bort alla autentiseringsuppgifter från ett tjänst huvud med ledning</span><span class="sxs-lookup"><span data-stu-id="a8eba-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="a8eba-119">Hämtar tjänstens huvud namn med objekt-ID ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' och pipes till Remove-AzADSpCredential cmdlet för att ta bort alla autentiseringsuppgifter från den tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="a8eba-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="a8eba-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8eba-120">PARAMETERS</span></span>

### <span data-ttu-id="a8eba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8eba-121">-DefaultProfile</span></span>
<span data-ttu-id="a8eba-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a8eba-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8eba-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a8eba-123">-DisplayName</span></span>
<span data-ttu-id="a8eba-124">Visnings namnet på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="a8eba-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="a8eba-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a8eba-125">-Force</span></span>
<span data-ttu-id="a8eba-126">Växla till att ta bort autentiseringsuppgiften utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a8eba-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="a8eba-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a8eba-127">-KeyId</span></span>
<span data-ttu-id="a8eba-128">Anger den autentiseringsinformation som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a8eba-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="a8eba-129">Huvud-ID: na för ett tjänst huvud konto kan erhållas med hjälp av Get-AzADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8eba-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="a8eba-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a8eba-130">-ObjectId</span></span>
<span data-ttu-id="a8eba-131">Objekt-ID för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="a8eba-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8eba-132">-PassThru</span></span>
<span data-ttu-id="a8eba-133">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="a8eba-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a8eba-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a8eba-134">-ServicePrincipalName</span></span>
<span data-ttu-id="a8eba-135">Namnet (SPN) för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="a8eba-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="a8eba-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="a8eba-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="a8eba-137">Tjänst huvud objekt som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="a8eba-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8eba-138">-Confirm</span></span>
<span data-ttu-id="a8eba-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8eba-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8eba-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8eba-140">-WhatIf</span></span>
<span data-ttu-id="a8eba-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8eba-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8eba-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8eba-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8eba-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8eba-143">CommonParameters</span></span>
<span data-ttu-id="a8eba-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8eba-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8eba-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8eba-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8eba-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8eba-146">INPUTS</span></span>

### <span data-ttu-id="a8eba-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a8eba-147">System.String</span></span>

### <span data-ttu-id="a8eba-148">Microsoft. Azure. commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a8eba-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="a8eba-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a8eba-149">System.Guid</span></span>

## <span data-ttu-id="a8eba-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8eba-150">OUTPUTS</span></span>

### <span data-ttu-id="a8eba-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8eba-151">System.Boolean</span></span>

## <span data-ttu-id="a8eba-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8eba-152">NOTES</span></span>

## <span data-ttu-id="a8eba-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8eba-153">RELATED LINKS</span></span>

[<span data-ttu-id="a8eba-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a8eba-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="a8eba-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a8eba-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="a8eba-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a8eba-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

