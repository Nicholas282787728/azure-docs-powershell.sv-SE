---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 766b4d3bd135295cddf3dd0c143519c3dde50b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575104"
---
# <span data-ttu-id="52135-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="52135-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="52135-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52135-102">SYNOPSIS</span></span>
<span data-ttu-id="52135-103">Tar bort Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="52135-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52135-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52135-104">SYNTAX</span></span>

### <span data-ttu-id="52135-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="52135-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52135-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52135-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52135-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="52135-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52135-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52135-108">InputObjectParameterSet</span></span>
```
Remove-AzureRmADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52135-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52135-109">DESCRIPTION</span></span>
<span data-ttu-id="52135-110">Tar bort Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="52135-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="52135-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52135-111">EXAMPLES</span></span>

### <span data-ttu-id="52135-112">Exempel 1 – ta bort program utifrån objekt-ID</span><span class="sxs-lookup"><span data-stu-id="52135-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="52135-113">Tar bort programmet med objekt-ID ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="52135-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="52135-114">Exempel 2 – ta bort program utifrån program-ID</span><span class="sxs-lookup"><span data-stu-id="52135-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="52135-115">Tar bort programmet med program-ID ' f9c5ea4f-28f0-401A-a491-491a037fa346 ' från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="52135-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="52135-116">Exempel 3 – ta bort program från rör</span><span class="sxs-lookup"><span data-stu-id="52135-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzureRmADApplication
```

<span data-ttu-id="52135-117">Hämtar programmet med objekt-ID ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' och pipes till Remove-AzureRmADApplication cmdlet för att ta bort programmet från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="52135-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzureRmADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="52135-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52135-118">PARAMETERS</span></span>

### <span data-ttu-id="52135-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="52135-119">-ApplicationId</span></span>
<span data-ttu-id="52135-120">Program-ID för programmet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="52135-120">The application id of the application to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52135-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52135-121">-DefaultProfile</span></span>
<span data-ttu-id="52135-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="52135-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52135-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="52135-123">-DisplayName</span></span>
<span data-ttu-id="52135-124">Programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="52135-124">The display name of the application.</span></span>

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

### <span data-ttu-id="52135-125">-Force</span><span class="sxs-lookup"><span data-stu-id="52135-125">-Force</span></span>
<span data-ttu-id="52135-126">Växla till att ta bort ett program utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="52135-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="52135-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52135-127">-InputObject</span></span>
<span data-ttu-id="52135-128">Objektet som representerar programmet du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="52135-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52135-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="52135-129">-ObjectId</span></span>
<span data-ttu-id="52135-130">Objekt-ID för programmet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="52135-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="52135-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52135-131">-PassThru</span></span>
<span data-ttu-id="52135-132">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="52135-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="52135-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52135-133">-Confirm</span></span>
<span data-ttu-id="52135-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52135-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52135-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52135-135">-WhatIf</span></span>
<span data-ttu-id="52135-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52135-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52135-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52135-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52135-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52135-138">CommonParameters</span></span>
<span data-ttu-id="52135-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52135-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52135-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52135-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52135-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52135-141">INPUTS</span></span>

### <span data-ttu-id="52135-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="52135-142">System.Guid</span></span>

### <span data-ttu-id="52135-143">System. String</span><span class="sxs-lookup"><span data-stu-id="52135-143">System.String</span></span>

### <span data-ttu-id="52135-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="52135-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="52135-145">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52135-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="52135-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52135-146">OUTPUTS</span></span>

### <span data-ttu-id="52135-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52135-147">System.Boolean</span></span>

## <span data-ttu-id="52135-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52135-148">NOTES</span></span>
<span data-ttu-id="52135-149">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="52135-149">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="52135-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52135-150">RELATED LINKS</span></span>

[<span data-ttu-id="52135-151">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="52135-151">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="52135-152">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="52135-152">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="52135-153">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="52135-153">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="52135-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="52135-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

