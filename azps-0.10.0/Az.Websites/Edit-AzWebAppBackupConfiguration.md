---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/edit-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: cfac8f1cd3d25ff630900bb5d7723e713b3d4c65
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923398"
---
# <span data-ttu-id="a40f2-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a40f2-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="a40f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a40f2-102">SYNOPSIS</span></span>

## <span data-ttu-id="a40f2-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a40f2-103">SYNTAX</span></span>

### <span data-ttu-id="a40f2-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a40f2-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="a40f2-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a40f2-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="a40f2-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a40f2-106">DESCRIPTION</span></span>
<span data-ttu-id="a40f2-107">Cmdleten **Edit-AzWebAppBackupConfiguration** redigerar den aktuella konfigurations säkerhets kopian för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a40f2-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="a40f2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a40f2-108">EXAMPLES</span></span>

## <span data-ttu-id="a40f2-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a40f2-109">PARAMETERS</span></span>

### <span data-ttu-id="a40f2-110">-Databaser</span><span class="sxs-lookup"><span data-stu-id="a40f2-110">-Databases</span></span>
<span data-ttu-id="a40f2-111">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="a40f2-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40f2-112">-DefaultProfile</span></span>
<span data-ttu-id="a40f2-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a40f2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="a40f2-114">-FrequencyInterval</span></span>
<span data-ttu-id="a40f2-115">Frekvens intervall</span><span class="sxs-lookup"><span data-stu-id="a40f2-115">Frequency Interval</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="a40f2-116">-FrequencyUnit</span></span>
<span data-ttu-id="a40f2-117">Frekvens enhet</span><span class="sxs-lookup"><span data-stu-id="a40f2-117">Frequency Unit</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="a40f2-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="a40f2-119">Behåll minst ett säkerhets kopierings alternativ</span><span class="sxs-lookup"><span data-stu-id="a40f2-119">Keep At Least One Backup Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a40f2-120">-Name</span></span>
<span data-ttu-id="a40f2-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="a40f2-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a40f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="a40f2-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a40f2-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a40f2-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="a40f2-125">Kvarhållningsperiod i dagar</span><span class="sxs-lookup"><span data-stu-id="a40f2-125">Retention Period In Days</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="a40f2-126">-Slot</span></span>
<span data-ttu-id="a40f2-127">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="a40f2-127">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a40f2-128">-StartTime</span></span>
<span data-ttu-id="a40f2-129">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="a40f2-129">StartTime in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="a40f2-130">-StorageAccountUrl</span></span>
<span data-ttu-id="a40f2-131">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="a40f2-131">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a40f2-132">-WebApp</span></span>
<span data-ttu-id="a40f2-133">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="a40f2-133">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40f2-134">CommonParameters</span></span>
<span data-ttu-id="a40f2-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40f2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40f2-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40f2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40f2-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a40f2-137">INPUTS</span></span>

### <span data-ttu-id="a40f2-138">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="a40f2-138">Site</span></span>
<span data-ttu-id="a40f2-139">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a40f2-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a40f2-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a40f2-140">OUTPUTS</span></span>

### <span data-ttu-id="a40f2-141">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a40f2-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="a40f2-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a40f2-142">NOTES</span></span>

## <span data-ttu-id="a40f2-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a40f2-143">RELATED LINKS</span></span>

[<span data-ttu-id="a40f2-144">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a40f2-144">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


