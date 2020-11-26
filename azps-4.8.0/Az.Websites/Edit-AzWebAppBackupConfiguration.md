---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 9cf7974cb284052fab0dd6c8cb27409543db272c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262388"
---
# <span data-ttu-id="628ee-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="628ee-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="628ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="628ee-102">SYNOPSIS</span></span>

## <span data-ttu-id="628ee-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="628ee-103">SYNTAX</span></span>

### <span data-ttu-id="628ee-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="628ee-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="628ee-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="628ee-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="628ee-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="628ee-106">DESCRIPTION</span></span>
<span data-ttu-id="628ee-107">Cmdleten **Edit-AzWebAppBackupConfiguration** redigerar den aktuella konfigurations säkerhets kopian för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="628ee-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="628ee-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="628ee-108">EXAMPLES</span></span>

### <span data-ttu-id="628ee-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="628ee-109">Example 1</span></span>

<span data-ttu-id="628ee-110">Edit-AzWebAppBackupConfiguration cmdlet redigerar den aktuella konfigurations säkerhets kopian för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="628ee-110">The Edit-AzWebAppBackupConfiguration cmdlet edits the current configuration backup for an Azure Web App.</span></span> <span data-ttu-id="628ee-111">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="628ee-111">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Edit-AzWebAppBackupConfiguration -FrequencyInterval <Int32> -FrequencyUnit <String> -KeepAtLeastOneBackup -Name IpRule -ResourceGroupName MyResourceGroup -RetentionPeriodInDays <Int32> -StartTime 2016-11-30T22:00:00Z -StorageAccountUrl 'https://storageaccount.file.core.windows.net'
```

## <span data-ttu-id="628ee-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="628ee-112">PARAMETERS</span></span>

### <span data-ttu-id="628ee-113">-Databaser</span><span class="sxs-lookup"><span data-stu-id="628ee-113">-Databases</span></span>
<span data-ttu-id="628ee-114">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="628ee-114">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="628ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="628ee-115">-DefaultProfile</span></span>
<span data-ttu-id="628ee-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="628ee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="628ee-117">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="628ee-117">-FrequencyInterval</span></span>
<span data-ttu-id="628ee-118">Frekvens intervall</span><span class="sxs-lookup"><span data-stu-id="628ee-118">Frequency Interval</span></span>

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

### <span data-ttu-id="628ee-119">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="628ee-119">-FrequencyUnit</span></span>
<span data-ttu-id="628ee-120">Frekvens enhet</span><span class="sxs-lookup"><span data-stu-id="628ee-120">Frequency Unit</span></span>

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

### <span data-ttu-id="628ee-121">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="628ee-121">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="628ee-122">Behåll minst ett säkerhets kopierings alternativ</span><span class="sxs-lookup"><span data-stu-id="628ee-122">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="628ee-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="628ee-123">-Name</span></span>
<span data-ttu-id="628ee-124">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="628ee-124">WebApp Name</span></span>

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

### <span data-ttu-id="628ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="628ee-125">-ResourceGroupName</span></span>
<span data-ttu-id="628ee-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="628ee-126">Resource Group Name</span></span>

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

### <span data-ttu-id="628ee-127">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="628ee-127">-RetentionPeriodInDays</span></span>
<span data-ttu-id="628ee-128">Kvarhållningsperiod i dagar</span><span class="sxs-lookup"><span data-stu-id="628ee-128">Retention Period In Days</span></span>

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

### <span data-ttu-id="628ee-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="628ee-129">-Slot</span></span>
<span data-ttu-id="628ee-130">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="628ee-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="628ee-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="628ee-131">-StartTime</span></span>
<span data-ttu-id="628ee-132">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="628ee-132">StartTime in UTC</span></span>

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

### <span data-ttu-id="628ee-133">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="628ee-133">-StorageAccountUrl</span></span>
<span data-ttu-id="628ee-134">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="628ee-134">Storage Account Url</span></span>

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

### <span data-ttu-id="628ee-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="628ee-135">-WebApp</span></span>
<span data-ttu-id="628ee-136">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="628ee-136">WebApp Object</span></span>

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

### <span data-ttu-id="628ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="628ee-137">CommonParameters</span></span>
<span data-ttu-id="628ee-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="628ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="628ee-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="628ee-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="628ee-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="628ee-140">INPUTS</span></span>

### <span data-ttu-id="628ee-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="628ee-141">System.Int32</span></span>

### <span data-ttu-id="628ee-142">System. String</span><span class="sxs-lookup"><span data-stu-id="628ee-142">System.String</span></span>

### <span data-ttu-id="628ee-143">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="628ee-143">System.DateTime</span></span>

### <span data-ttu-id="628ee-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="628ee-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="628ee-145">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="628ee-145">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="628ee-146">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="628ee-146">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="628ee-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="628ee-147">OUTPUTS</span></span>

### <span data-ttu-id="628ee-148">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="628ee-148">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="628ee-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="628ee-149">NOTES</span></span>

## <span data-ttu-id="628ee-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="628ee-150">RELATED LINKS</span></span>

[<span data-ttu-id="628ee-151">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="628ee-151">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)

