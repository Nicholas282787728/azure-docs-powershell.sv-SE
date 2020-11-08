---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 490f7b4a0cb723d02deb1d18e8a2ddfb993e7f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089403"
---
# <span data-ttu-id="67087-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="67087-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="67087-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67087-102">SYNOPSIS</span></span>

## <span data-ttu-id="67087-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67087-103">SYNTAX</span></span>

### <span data-ttu-id="67087-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="67087-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="67087-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="67087-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="67087-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67087-106">DESCRIPTION</span></span>
<span data-ttu-id="67087-107">Cmdleten **Edit-AzWebAppBackupConfiguration** redigerar den aktuella konfigurations säkerhets kopian för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="67087-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="67087-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67087-108">EXAMPLES</span></span>

## <span data-ttu-id="67087-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67087-109">PARAMETERS</span></span>

### <span data-ttu-id="67087-110">-Databaser</span><span class="sxs-lookup"><span data-stu-id="67087-110">-Databases</span></span>
<span data-ttu-id="67087-111">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="67087-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="67087-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67087-112">-DefaultProfile</span></span>
<span data-ttu-id="67087-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67087-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67087-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="67087-114">-FrequencyInterval</span></span>
<span data-ttu-id="67087-115">Frekvens intervall</span><span class="sxs-lookup"><span data-stu-id="67087-115">Frequency Interval</span></span>

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

### <span data-ttu-id="67087-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="67087-116">-FrequencyUnit</span></span>
<span data-ttu-id="67087-117">Frekvens enhet</span><span class="sxs-lookup"><span data-stu-id="67087-117">Frequency Unit</span></span>

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

### <span data-ttu-id="67087-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="67087-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="67087-119">Behåll minst ett säkerhets kopierings alternativ</span><span class="sxs-lookup"><span data-stu-id="67087-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="67087-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="67087-120">-Name</span></span>
<span data-ttu-id="67087-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="67087-121">WebApp Name</span></span>

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

### <span data-ttu-id="67087-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67087-122">-ResourceGroupName</span></span>
<span data-ttu-id="67087-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="67087-123">Resource Group Name</span></span>

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

### <span data-ttu-id="67087-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="67087-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="67087-125">Kvarhållningsperiod i dagar</span><span class="sxs-lookup"><span data-stu-id="67087-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="67087-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="67087-126">-Slot</span></span>
<span data-ttu-id="67087-127">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="67087-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="67087-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="67087-128">-StartTime</span></span>
<span data-ttu-id="67087-129">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="67087-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="67087-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="67087-130">-StorageAccountUrl</span></span>
<span data-ttu-id="67087-131">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="67087-131">Storage Account Url</span></span>

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

### <span data-ttu-id="67087-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="67087-132">-WebApp</span></span>
<span data-ttu-id="67087-133">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="67087-133">WebApp Object</span></span>

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

### <span data-ttu-id="67087-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67087-134">CommonParameters</span></span>
<span data-ttu-id="67087-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67087-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67087-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67087-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67087-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67087-137">INPUTS</span></span>

### <span data-ttu-id="67087-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="67087-138">System.Int32</span></span>

### <span data-ttu-id="67087-139">System. String</span><span class="sxs-lookup"><span data-stu-id="67087-139">System.String</span></span>

### <span data-ttu-id="67087-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="67087-140">System.DateTime</span></span>

### <span data-ttu-id="67087-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="67087-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="67087-142">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="67087-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="67087-143">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="67087-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="67087-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67087-144">OUTPUTS</span></span>

### <span data-ttu-id="67087-145">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="67087-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="67087-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67087-146">NOTES</span></span>

## <span data-ttu-id="67087-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67087-147">RELATED LINKS</span></span>

[<span data-ttu-id="67087-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="67087-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


