---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923150"
---
# <span data-ttu-id="eddef-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="eddef-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="eddef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eddef-102">SYNOPSIS</span></span>
<span data-ttu-id="eddef-103">Ta bort ett specifikt Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="eddef-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="eddef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eddef-104">SYNTAX</span></span>

### <span data-ttu-id="eddef-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="eddef-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eddef-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eddef-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eddef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eddef-107">DESCRIPTION</span></span>
<span data-ttu-id="eddef-108">Ta bort ett specifikt Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="eddef-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="eddef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eddef-109">EXAMPLES</span></span>

### <span data-ttu-id="eddef-110">Exempel 1: Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="eddef-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="eddef-111">Tar bort TestUbuntu. test. 1.0.0 från Azure Stack Gallery.</span><span class="sxs-lookup"><span data-stu-id="eddef-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="eddef-112">Exempel 2: Remove-AzsGalleryItem via pipeline</span><span class="sxs-lookup"><span data-stu-id="eddef-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="eddef-113">Tar bort TestUbuntu. test. 1.0.0 via pipeline.</span><span class="sxs-lookup"><span data-stu-id="eddef-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="eddef-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eddef-114">PARAMETERS</span></span>

### <span data-ttu-id="eddef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eddef-115">-DefaultProfile</span></span>
<span data-ttu-id="eddef-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eddef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eddef-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eddef-117">-InputObject</span></span>
<span data-ttu-id="eddef-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="eddef-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="eddef-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="eddef-119">-Name</span></span>
<span data-ttu-id="eddef-120">Identitet för GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="eddef-120">Identity of the gallery item.</span></span>
<span data-ttu-id="eddef-121">Inkluderar Publisher-namn, artikel namn och kan innehålla version avgränsad efter period tecken.</span><span class="sxs-lookup"><span data-stu-id="eddef-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eddef-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eddef-122">-PassThru</span></span>
<span data-ttu-id="eddef-123">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="eddef-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eddef-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eddef-124">-SubscriptionId</span></span>
<span data-ttu-id="eddef-125">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="eddef-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eddef-126">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="eddef-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eddef-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eddef-127">-Confirm</span></span>
<span data-ttu-id="eddef-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eddef-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eddef-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eddef-129">-WhatIf</span></span>
<span data-ttu-id="eddef-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eddef-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eddef-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eddef-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eddef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eddef-132">CommonParameters</span></span>
<span data-ttu-id="eddef-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eddef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eddef-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eddef-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eddef-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eddef-135">INPUTS</span></span>

### <span data-ttu-id="eddef-136">Microsoft. Azure. PowerShell. cmdlets. Gallery. Models. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="eddef-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="eddef-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eddef-137">OUTPUTS</span></span>

### <span data-ttu-id="eddef-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eddef-138">System.Boolean</span></span>



## <span data-ttu-id="eddef-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eddef-139">NOTES</span></span>

<span data-ttu-id="eddef-140">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="eddef-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eddef-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eddef-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="eddef-142">INPUTOBJECT <IGalleryIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="eddef-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eddef-143">`[GalleryItemName <String>]`: ID för GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="eddef-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="eddef-144">Inkluderar Publisher-namn, artikel namn och kan innehålla version avgränsad efter period tecken.</span><span class="sxs-lookup"><span data-stu-id="eddef-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="eddef-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="eddef-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eddef-146">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="eddef-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eddef-147">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="eddef-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="eddef-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eddef-148">RELATED LINKS</span></span>

