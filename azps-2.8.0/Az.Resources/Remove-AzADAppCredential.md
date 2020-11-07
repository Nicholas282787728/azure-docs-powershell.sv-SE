---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 5c47e707c3421c6efc1998e55897f6bb9be8fa65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919290"
---
# <span data-ttu-id="60a6c-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="60a6c-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="60a6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="60a6c-103">Tar bort en autentiseringsuppgift från ett program.</span><span class="sxs-lookup"><span data-stu-id="60a6c-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="60a6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60a6c-104">SYNTAX</span></span>

### <span data-ttu-id="60a6c-105">ApplicationObjectIdWithKeyIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="60a6c-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a6c-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60a6c-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a6c-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="60a6c-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a6c-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60a6c-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60a6c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60a6c-109">DESCRIPTION</span></span>
<span data-ttu-id="60a6c-110">Remove-AzADAppCredential cmdleten kan användas för att ta bort en autentiseringsinformation från ett program om det rör sig om ett problem eller när förnyelsen av autentiseringsuppgiften förnyas.</span><span class="sxs-lookup"><span data-stu-id="60a6c-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="60a6c-111">Programmet identifieras genom att ange objekt-ID: t eller AppId.</span><span class="sxs-lookup"><span data-stu-id="60a6c-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="60a6c-112">Den autentiseringsuppgift som ska tas bort identifieras via dess ID.</span><span class="sxs-lookup"><span data-stu-id="60a6c-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="60a6c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60a6c-113">EXAMPLES</span></span>

### <span data-ttu-id="60a6c-114">Exempel 1 – ta bort en specifik autentiseringsuppgift från ett program</span><span class="sxs-lookup"><span data-stu-id="60a6c-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="60a6c-115">Tar bort autentiseringsuppgiften med ID ' 9044423a-60a3-45ac-9ab1-09534157ebb ' från programmet med objekt-ID ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 '.</span><span class="sxs-lookup"><span data-stu-id="60a6c-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="60a6c-116">Exempel 2 – ta bort alla autentiseringsuppgifter från ett program</span><span class="sxs-lookup"><span data-stu-id="60a6c-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="60a6c-117">Tar bort alla autentiseringsuppgifter från programmet med program-ID ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 '.</span><span class="sxs-lookup"><span data-stu-id="60a6c-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="60a6c-118">Exempel 3 – ta bort alla uppgifter med hjälp av rör</span><span class="sxs-lookup"><span data-stu-id="60a6c-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="60a6c-119">Hämtar programmet med objekt-ID ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' och pipes till Remove-AzADAppCredential cmdlet och tar bort alla autentiseringsuppgifter från det programmet.</span><span class="sxs-lookup"><span data-stu-id="60a6c-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="60a6c-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60a6c-120">PARAMETERS</span></span>

### <span data-ttu-id="60a6c-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="60a6c-121">-ApplicationId</span></span>
<span data-ttu-id="60a6c-122">ID för programmet som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="60a6c-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a6c-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="60a6c-123">-ApplicationObject</span></span>
<span data-ttu-id="60a6c-124">Programobjektet som uppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="60a6c-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60a6c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a6c-125">-DefaultProfile</span></span>
<span data-ttu-id="60a6c-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="60a6c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60a6c-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="60a6c-127">-DisplayName</span></span>
<span data-ttu-id="60a6c-128">Programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="60a6c-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a6c-129">-Force</span><span class="sxs-lookup"><span data-stu-id="60a6c-129">-Force</span></span>
<span data-ttu-id="60a6c-130">Växla till att ta bort autentiseringsuppgiften utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="60a6c-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="60a6c-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="60a6c-131">-KeyId</span></span>
<span data-ttu-id="60a6c-132">Anger den autentiseringsinformation som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="60a6c-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="60a6c-133">De viktigaste ID: na för programmet kan erhållas med hjälp av Get-AzADAppCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a6c-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a6c-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="60a6c-134">-ObjectId</span></span>
<span data-ttu-id="60a6c-135">Objekt-ID för programmet som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="60a6c-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a6c-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60a6c-136">-PassThru</span></span>
<span data-ttu-id="60a6c-137">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="60a6c-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="60a6c-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="60a6c-138">-Confirm</span></span>
<span data-ttu-id="60a6c-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="60a6c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a6c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a6c-140">-WhatIf</span></span>
<span data-ttu-id="60a6c-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="60a6c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a6c-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="60a6c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a6c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a6c-143">CommonParameters</span></span>
<span data-ttu-id="60a6c-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a6c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a6c-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a6c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a6c-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60a6c-146">INPUTS</span></span>

### <span data-ttu-id="60a6c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="60a6c-147">System.String</span></span>

### <span data-ttu-id="60a6c-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="60a6c-148">System.Guid</span></span>

### <span data-ttu-id="60a6c-149">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="60a6c-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="60a6c-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60a6c-150">OUTPUTS</span></span>

### <span data-ttu-id="60a6c-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60a6c-151">System.Boolean</span></span>

## <span data-ttu-id="60a6c-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60a6c-152">NOTES</span></span>

## <span data-ttu-id="60a6c-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60a6c-153">RELATED LINKS</span></span>

[<span data-ttu-id="60a6c-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="60a6c-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="60a6c-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="60a6c-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="60a6c-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="60a6c-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
