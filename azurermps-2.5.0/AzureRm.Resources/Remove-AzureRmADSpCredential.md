---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: 73fff5ff4cf612c39bacd26fed61c4e856e34128
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928678"
---
# <span data-ttu-id="b2b8f-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b2b8f-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="b2b8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b8f-103">Tar bort en autentiseringsuppgift från ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2b8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2b8f-104">SYNTAX</span></span>

### <span data-ttu-id="b2b8f-105">ObjectIdWithKeyIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b2b8f-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2b8f-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2b8f-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2b8f-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2b8f-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2b8f-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2b8f-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2b8f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2b8f-109">DESCRIPTION</span></span>
<span data-ttu-id="b2b8f-110">Du kan använda Remove-AzureRmADSpCredential cmdlet för att ta bort en behörighets nycklar från ett säkerhets objekt om det rör sig om en kompromiss eller en del av förnyelsen av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="b2b8f-111">Tjänstens huvud namn identifieras genom att ange antingen objekt-ID eller SPN (Service Principal Name).</span><span class="sxs-lookup"><span data-stu-id="b2b8f-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="b2b8f-112">Den autentiseringsuppgift som ska tas bort identifieras via dess tillhör ande ID om en enskild autentiseringsuppgift ska tas bort eller med en "alla"-växel för att ta bort alla autentiseringsuppgifter som är kopplade till tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="b2b8f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2b8f-113">EXAMPLES</span></span>

### <span data-ttu-id="b2b8f-114">Exempel 1 – ta bort en specifik autentiseringsuppgift från ett SPN-namn</span><span class="sxs-lookup"><span data-stu-id="b2b8f-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="b2b8f-115">Tar bort autentiseringsuppgiften med ID ' 9044423a-60a3-45ac-9ab1-09534157ebb ' från tjänstens huvud namn med objekt-ID ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 '.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="b2b8f-116">Exempel 2 – ta bort alla autentiseringsuppgifter från ett huvud säkerhets objekt</span><span class="sxs-lookup"><span data-stu-id="b2b8f-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="b2b8f-117">Tar bort alla autentiseringsuppgifter från tjänstens huvud konto med SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="b2b8f-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="b2b8f-118">Exempel 3 – ta bort alla autentiseringsuppgifter från ett tjänst huvud med ledning</span><span class="sxs-lookup"><span data-stu-id="b2b8f-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADSpCredential
```

<span data-ttu-id="b2b8f-119">Hämtar tjänstens huvud namn med objekt-ID ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' och pipes till Remove-AzureRmADSpCredential cmdlet för att ta bort alla autentiseringsuppgifter från den tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="b2b8f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2b8f-120">PARAMETERS</span></span>

### <span data-ttu-id="b2b8f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b8f-121">-DefaultProfile</span></span>
<span data-ttu-id="b2b8f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b2b8f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2b8f-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b2b8f-123">-DisplayName</span></span>
<span data-ttu-id="b2b8f-124">Visnings namnet på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="b2b8f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b2b8f-125">-Force</span></span>
<span data-ttu-id="b2b8f-126">Växla till att ta bort autentiseringsuppgiften utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="b2b8f-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b2b8f-127">-KeyId</span></span>
<span data-ttu-id="b2b8f-128">Anger den autentiseringsinformation som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="b2b8f-129">Huvud-ID: na för ett tjänst huvud konto kan erhållas med hjälp av Get-AzureRmADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="b2b8f-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b2b8f-130">-ObjectId</span></span>
<span data-ttu-id="b2b8f-131">Objekt-ID för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-131">The object id of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="b2b8f-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2b8f-132">-PassThru</span></span>
<span data-ttu-id="b2b8f-133">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b2b8f-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b2b8f-134">-ServicePrincipalName</span></span>
<span data-ttu-id="b2b8f-135">Namnet (SPN) för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="b2b8f-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="b2b8f-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="b2b8f-137">Tjänst huvud objekt som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-137">The service principal object to remove the credentials from.</span></span>

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

### <span data-ttu-id="b2b8f-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b2b8f-138">-Confirm</span></span>
<span data-ttu-id="b2b8f-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2b8f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2b8f-140">-WhatIf</span></span>
<span data-ttu-id="b2b8f-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2b8f-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2b8f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b8f-143">CommonParameters</span></span>
<span data-ttu-id="b2b8f-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b8f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b8f-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2b8f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b8f-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2b8f-146">INPUTS</span></span>

### <span data-ttu-id="b2b8f-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b2b8f-147">System.Guid</span></span>

### <span data-ttu-id="b2b8f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b2b8f-148">System.String</span></span>

### <span data-ttu-id="b2b8f-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b2b8f-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="b2b8f-150">Parametrar: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b2b8f-150">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="b2b8f-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2b8f-151">OUTPUTS</span></span>

### <span data-ttu-id="b2b8f-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2b8f-152">System.Boolean</span></span>

## <span data-ttu-id="b2b8f-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2b8f-153">NOTES</span></span>

## <span data-ttu-id="b2b8f-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2b8f-154">RELATED LINKS</span></span>

[<span data-ttu-id="b2b8f-155">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b2b8f-155">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="b2b8f-156">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b2b8f-156">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="b2b8f-157">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b2b8f-157">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

