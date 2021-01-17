---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413347"
---
# <span data-ttu-id="af092-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="af092-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="af092-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af092-102">SYNOPSIS</span></span>
<span data-ttu-id="af092-103">Tar bort ett befintligt jobb.</span><span class="sxs-lookup"><span data-stu-id="af092-103">Deletes an existing job.</span></span>
<span data-ttu-id="af092-104">Det är bara jobb i tillståndet skapa eller slutfört som kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="af092-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="af092-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af092-105">SYNTAX</span></span>

### <span data-ttu-id="af092-106">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="af092-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="af092-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="af092-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af092-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af092-108">DESCRIPTION</span></span>
<span data-ttu-id="af092-109">Tar bort ett befintligt jobb.</span><span class="sxs-lookup"><span data-stu-id="af092-109">Deletes an existing job.</span></span>
<span data-ttu-id="af092-110">Det är bara jobb i tillståndet skapa eller slutfört som kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="af092-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="af092-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af092-111">EXAMPLES</span></span>

### <span data-ttu-id="af092-112">Exempel 1: ta bort ImportExport-jobbet genom resourceGroup och Server namn</span><span class="sxs-lookup"><span data-stu-id="af092-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="af092-113">Denna cmdlet tar bort ImportExport-jobbet genom resourceGroup och Server namn.</span><span class="sxs-lookup"><span data-stu-id="af092-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="af092-114">Exempel 2: ta bort ImportExport-jobbet efter identitet</span><span class="sxs-lookup"><span data-stu-id="af092-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="af092-115">Denna cmdlet tar bort ImportExport-jobbet efter identitet.</span><span class="sxs-lookup"><span data-stu-id="af092-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="af092-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af092-116">PARAMETERS</span></span>

### <span data-ttu-id="af092-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="af092-117">-AcceptLanguage</span></span>
<span data-ttu-id="af092-118">Anger önskat språk för svaret.</span><span class="sxs-lookup"><span data-stu-id="af092-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="af092-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af092-119">-DefaultProfile</span></span>
<span data-ttu-id="af092-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af092-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af092-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af092-121">-InputObject</span></span>
<span data-ttu-id="af092-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="af092-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af092-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="af092-123">-Name</span></span>
<span data-ttu-id="af092-124">Namnet på import-och export jobbet.</span><span class="sxs-lookup"><span data-stu-id="af092-124">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af092-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af092-125">-PassThru</span></span>
<span data-ttu-id="af092-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="af092-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="af092-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af092-127">-ResourceGroupName</span></span>
<span data-ttu-id="af092-128">Resurs gruppens namn identifierar unikt resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="af092-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af092-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af092-129">-SubscriptionId</span></span>
<span data-ttu-id="af092-130">Abonnemangs-ID för Azure-användaren.</span><span class="sxs-lookup"><span data-stu-id="af092-130">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af092-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af092-131">-Confirm</span></span>
<span data-ttu-id="af092-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af092-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af092-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af092-133">-WhatIf</span></span>
<span data-ttu-id="af092-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af092-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af092-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af092-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af092-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af092-136">CommonParameters</span></span>
<span data-ttu-id="af092-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af092-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af092-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af092-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af092-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af092-139">INPUTS</span></span>

### <span data-ttu-id="af092-140">Microsoft. Azure. PowerShell. cmdletar. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="af092-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="af092-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af092-141">OUTPUTS</span></span>

### <span data-ttu-id="af092-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af092-142">System.Boolean</span></span>

## <span data-ttu-id="af092-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af092-143">NOTES</span></span>

<span data-ttu-id="af092-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="af092-144">ALIASES</span></span>

<span data-ttu-id="af092-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="af092-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af092-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="af092-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af092-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="af092-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af092-148">INPUTOBJECT <IImportExportIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="af092-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="af092-149">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="af092-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="af092-150">`[JobName <String>]`: Import-och export jobbets namn.</span><span class="sxs-lookup"><span data-stu-id="af092-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="af092-151">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="af092-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="af092-152">Till exempel West, USA eller västkusten.</span><span class="sxs-lookup"><span data-stu-id="af092-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="af092-153">`[ResourceGroupName <String>]`: Resurs grupp namnet identifierar unikt resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="af092-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="af092-154">`[SubscriptionId <String>]`: Prenumerations-ID för Azure-användaren.</span><span class="sxs-lookup"><span data-stu-id="af092-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="af092-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af092-155">RELATED LINKS</span></span>

