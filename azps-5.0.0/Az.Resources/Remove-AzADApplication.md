---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: e27dcc838499e742c887f60a30021d8ac99277f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269784"
---
# <span data-ttu-id="8f513-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f513-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="8f513-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f513-102">SYNOPSIS</span></span>
<span data-ttu-id="8f513-103">Tar bort Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="8f513-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="8f513-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f513-104">SYNTAX</span></span>

### <span data-ttu-id="8f513-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8f513-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f513-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f513-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f513-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f513-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f513-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f513-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f513-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f513-109">DESCRIPTION</span></span>
<span data-ttu-id="8f513-110">Tar bort Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="8f513-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="8f513-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f513-111">EXAMPLES</span></span>

### <span data-ttu-id="8f513-112">Exempel 1: ta bort program utifrån objekt-ID</span><span class="sxs-lookup"><span data-stu-id="8f513-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="8f513-113">Tar bort programmet med objekt-ID ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="8f513-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="8f513-114">Exempel 2: ta bort program utifrån program-ID</span><span class="sxs-lookup"><span data-stu-id="8f513-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="8f513-115">Tar bort programmet med program-ID ' f9c5ea4f-28f0-401A-a491-491a037fa346 ' från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="8f513-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="8f513-116">Exempel 3: ta bort programmet med rör</span><span class="sxs-lookup"><span data-stu-id="8f513-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="8f513-117">Hämtar programmet med objekt-ID ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' och pipes till Remove-AzADApplication cmdlet för att ta bort programmet från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="8f513-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="8f513-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f513-118">PARAMETERS</span></span>

### <span data-ttu-id="8f513-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8f513-119">-ApplicationId</span></span>
<span data-ttu-id="8f513-120">Program-ID för programmet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8f513-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="8f513-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f513-121">-DefaultProfile</span></span>
<span data-ttu-id="8f513-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8f513-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f513-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8f513-123">-DisplayName</span></span>
<span data-ttu-id="8f513-124">Programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="8f513-124">The display name of the application.</span></span>

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

### <span data-ttu-id="8f513-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8f513-125">-Force</span></span>
<span data-ttu-id="8f513-126">Växla till att ta bort ett program utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8f513-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="8f513-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f513-127">-InputObject</span></span>
<span data-ttu-id="8f513-128">Objektet som representerar programmet du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="8f513-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f513-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8f513-129">-ObjectId</span></span>
<span data-ttu-id="8f513-130">Objekt-ID för programmet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8f513-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="8f513-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f513-131">-PassThru</span></span>
<span data-ttu-id="8f513-132">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="8f513-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8f513-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f513-133">-Confirm</span></span>
<span data-ttu-id="8f513-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f513-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f513-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f513-135">-WhatIf</span></span>
<span data-ttu-id="8f513-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f513-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f513-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f513-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f513-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f513-138">CommonParameters</span></span>
<span data-ttu-id="8f513-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f513-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f513-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f513-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f513-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f513-141">INPUTS</span></span>

### <span data-ttu-id="8f513-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8f513-142">System.String</span></span>

### <span data-ttu-id="8f513-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8f513-143">System.Guid</span></span>

### <span data-ttu-id="8f513-144">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8f513-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="8f513-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f513-145">OUTPUTS</span></span>

### <span data-ttu-id="8f513-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f513-146">System.Boolean</span></span>

## <span data-ttu-id="8f513-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f513-147">NOTES</span></span>
<span data-ttu-id="8f513-148">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="8f513-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8f513-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f513-149">RELATED LINKS</span></span>

[<span data-ttu-id="8f513-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f513-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="8f513-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f513-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="8f513-152">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f513-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="8f513-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8f513-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

