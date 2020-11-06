---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577724"
---
# <span data-ttu-id="765d0-101">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="765d0-101">Restore-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="765d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="765d0-102">SYNOPSIS</span></span>
<span data-ttu-id="765d0-103">Återställer en borttagen webbapp till en ny eller befintlig webbapp.</span><span class="sxs-lookup"><span data-stu-id="765d0-103">Restores a deleted web app to a new or existing web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="765d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="765d0-104">SYNTAX</span></span>

### <span data-ttu-id="765d0-105">FromDeletedResourceName</span><span class="sxs-lookup"><span data-stu-id="765d0-105">FromDeletedResourceName</span></span>
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="765d0-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="765d0-106">FromDeletedApp</span></span>
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## <span data-ttu-id="765d0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="765d0-107">DESCRIPTION</span></span>
<span data-ttu-id="765d0-108">Cmdleten **restore-AzureRmDeletedWebApp** återställer en borttagen webbapp.</span><span class="sxs-lookup"><span data-stu-id="765d0-108">The **Restore-AzureRmDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="765d0-109">Webb programmet som anges av TargetResourceGroupName, TargetName och TargetSlot kommer att skrivas över med innehållet och inställningarna för det borttagna webb programmet.</span><span class="sxs-lookup"><span data-stu-id="765d0-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="765d0-110">Om mål parametrarna inte anges fylls de automatiskt i med webb programmets resurs grupp, namn och plats.</span><span class="sxs-lookup"><span data-stu-id="765d0-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="765d0-111">Om mål webb programmet inte finns kommer det att skapas automatiskt i den app service-plan som anges av TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="765d0-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="765d0-112">Växeln RestoreContentOnly kan bara användas för att återställa de borttagna apparnas filer utan appinställningar.</span><span class="sxs-lookup"><span data-stu-id="765d0-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="765d0-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="765d0-113">EXAMPLES</span></span>

### <span data-ttu-id="765d0-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="765d0-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="765d0-115">Återställer en borttagen app som heter ContosoApp som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="765d0-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="765d0-116">En ny app med samma namn och resurs grupp kommer att skapas i App Service-planen med namnet ContosoPlan och den borttagna appens filer och inställningar återställs.</span><span class="sxs-lookup"><span data-stu-id="765d0-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="765d0-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="765d0-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="765d0-118">Återställer mellanlagrings platsen för en borttagen app som heter ContosoApp som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="765d0-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="765d0-119">Webb programmet som heter ContosoRestore som tillhör resurs gruppens standard-webeast skrivs över.</span><span class="sxs-lookup"><span data-stu-id="765d0-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="765d0-120">De borttagna webbappens inställningar återställs inte.</span><span class="sxs-lookup"><span data-stu-id="765d0-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="765d0-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="765d0-121">PARAMETERS</span></span>

### <span data-ttu-id="765d0-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="765d0-122">-AsJob</span></span>
<span data-ttu-id="765d0-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="765d0-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="765d0-124">-DefaultProfile</span></span>
<span data-ttu-id="765d0-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="765d0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-126">-Force</span><span class="sxs-lookup"><span data-stu-id="765d0-126">-Force</span></span>
<span data-ttu-id="765d0-127">Utför återställningen utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="765d0-127">Do the restore without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="765d0-128">-InputObject</span></span>
<span data-ttu-id="765d0-129">Den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="765d0-129">The deleted Azure Web App.</span></span>

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="765d0-130">-Name</span></span>
<span data-ttu-id="765d0-131">Namnet på den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="765d0-131">The name of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="765d0-132">-ResourceGroupName</span></span>
<span data-ttu-id="765d0-133">Resurs gruppen för den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="765d0-133">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="765d0-134">-RestoreContentOnly</span></span>
<span data-ttu-id="765d0-135">Återställ webbappens filer, men Återställ inte inställningarna.</span><span class="sxs-lookup"><span data-stu-id="765d0-135">Restore the web app's files, but do not restore the settings.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="765d0-136">-Slot</span></span>
<span data-ttu-id="765d0-137">Den borttagna Azure Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="765d0-137">The deleted Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="765d0-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="765d0-139">App Service-abonnemanget för den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="765d0-139">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="765d0-140">-TargetName</span></span>
<span data-ttu-id="765d0-141">Namnet på den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="765d0-141">The name of the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="765d0-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="765d0-143">Resurs gruppen som innehåller den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="765d0-143">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="765d0-144">-TargetSlot</span></span>
<span data-ttu-id="765d0-145">Namnet på den nya Azure Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="765d0-145">The name of the new Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765d0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="765d0-146">CommonParameters</span></span>
<span data-ttu-id="765d0-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="765d0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="765d0-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="765d0-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="765d0-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="765d0-149">INPUTS</span></span>

### <span data-ttu-id="765d0-150">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="765d0-150">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="765d0-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="765d0-151">OUTPUTS</span></span>

### <span data-ttu-id="765d0-152">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="765d0-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="765d0-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="765d0-153">NOTES</span></span>

## <span data-ttu-id="765d0-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="765d0-154">RELATED LINKS</span></span>

[<span data-ttu-id="765d0-155">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="765d0-155">Get-AzureRmDeletedWebApp</span></span>](./Get-AzureRmDeletedWebApp.md)
