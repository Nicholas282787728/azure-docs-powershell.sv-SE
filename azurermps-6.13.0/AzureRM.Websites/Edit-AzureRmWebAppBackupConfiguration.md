---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: a7a66197752e7dd9ec58e7eeca921af277687ed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573829"
---
# <span data-ttu-id="66e7d-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="66e7d-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="66e7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66e7d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66e7d-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66e7d-103">SYNTAX</span></span>

### <span data-ttu-id="66e7d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="66e7d-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="66e7d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="66e7d-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="66e7d-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66e7d-106">DESCRIPTION</span></span>
<span data-ttu-id="66e7d-107">Cmdleten **Edit-AzureRmWebAppBackupConfiguration** redigerar den aktuella konfigurations säkerhets kopian för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="66e7d-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="66e7d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66e7d-108">EXAMPLES</span></span>

## <span data-ttu-id="66e7d-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66e7d-109">PARAMETERS</span></span>

### <span data-ttu-id="66e7d-110">-Databaser</span><span class="sxs-lookup"><span data-stu-id="66e7d-110">-Databases</span></span>
<span data-ttu-id="66e7d-111">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="66e7d-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e7d-112">-DefaultProfile</span></span>
<span data-ttu-id="66e7d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66e7d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66e7d-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="66e7d-114">-FrequencyInterval</span></span>
<span data-ttu-id="66e7d-115">Frekvens intervall</span><span class="sxs-lookup"><span data-stu-id="66e7d-115">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="66e7d-116">-FrequencyUnit</span></span>
<span data-ttu-id="66e7d-117">Frekvens enhet</span><span class="sxs-lookup"><span data-stu-id="66e7d-117">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="66e7d-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="66e7d-119">Behåll minst ett säkerhets kopierings alternativ</span><span class="sxs-lookup"><span data-stu-id="66e7d-119">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="66e7d-120">-Name</span></span>
<span data-ttu-id="66e7d-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="66e7d-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66e7d-122">-ResourceGroupName</span></span>
<span data-ttu-id="66e7d-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="66e7d-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="66e7d-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="66e7d-125">Kvarhållningsperiod i dagar</span><span class="sxs-lookup"><span data-stu-id="66e7d-125">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="66e7d-126">-Slot</span></span>
<span data-ttu-id="66e7d-127">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="66e7d-127">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="66e7d-128">-StartTime</span></span>
<span data-ttu-id="66e7d-129">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="66e7d-129">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="66e7d-130">-StorageAccountUrl</span></span>
<span data-ttu-id="66e7d-131">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="66e7d-131">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="66e7d-132">-WebApp</span></span>
<span data-ttu-id="66e7d-133">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="66e7d-133">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66e7d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e7d-134">CommonParameters</span></span>
<span data-ttu-id="66e7d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66e7d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e7d-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66e7d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e7d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66e7d-137">INPUTS</span></span>

### <span data-ttu-id="66e7d-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="66e7d-138">System.Int32</span></span>

### <span data-ttu-id="66e7d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="66e7d-139">System.String</span></span>

### <span data-ttu-id="66e7d-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="66e7d-140">System.DateTime</span></span>

### <span data-ttu-id="66e7d-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66e7d-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="66e7d-142">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="66e7d-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="66e7d-143">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="66e7d-143">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="66e7d-144">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="66e7d-144">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="66e7d-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66e7d-145">OUTPUTS</span></span>

### <span data-ttu-id="66e7d-146">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="66e7d-146">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="66e7d-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66e7d-147">NOTES</span></span>

## <span data-ttu-id="66e7d-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66e7d-148">RELATED LINKS</span></span>

[<span data-ttu-id="66e7d-149">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="66e7d-149">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


