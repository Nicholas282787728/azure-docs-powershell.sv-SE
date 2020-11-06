---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 9c23484fa5f8b45548985645db45872fcc63f66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581884"
---
# <span data-ttu-id="88528-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="88528-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="88528-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88528-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88528-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88528-103">SYNTAX</span></span>

### <span data-ttu-id="88528-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="88528-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="88528-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="88528-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="88528-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88528-106">DESCRIPTION</span></span>
<span data-ttu-id="88528-107">Cmdleten **Edit-AzureRmWebAppBackupConfiguration** redigerar den aktuella konfigurations säkerhets kopian för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="88528-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="88528-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88528-108">EXAMPLES</span></span>

## <span data-ttu-id="88528-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88528-109">PARAMETERS</span></span>

### <span data-ttu-id="88528-110">-Databaser</span><span class="sxs-lookup"><span data-stu-id="88528-110">-Databases</span></span>
<span data-ttu-id="88528-111">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="88528-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="88528-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88528-112">-DefaultProfile</span></span>
<span data-ttu-id="88528-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="88528-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88528-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="88528-114">-FrequencyInterval</span></span>
<span data-ttu-id="88528-115">Frekvens intervall</span><span class="sxs-lookup"><span data-stu-id="88528-115">Frequency Interval</span></span>

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

### <span data-ttu-id="88528-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="88528-116">-FrequencyUnit</span></span>
<span data-ttu-id="88528-117">Frekvens enhet</span><span class="sxs-lookup"><span data-stu-id="88528-117">Frequency Unit</span></span>

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

### <span data-ttu-id="88528-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="88528-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="88528-119">Behåll minst ett säkerhets kopierings alternativ</span><span class="sxs-lookup"><span data-stu-id="88528-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="88528-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="88528-120">-Name</span></span>
<span data-ttu-id="88528-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="88528-121">WebApp Name</span></span>

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

### <span data-ttu-id="88528-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88528-122">-ResourceGroupName</span></span>
<span data-ttu-id="88528-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="88528-123">Resource Group Name</span></span>

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

### <span data-ttu-id="88528-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="88528-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="88528-125">Kvarhållningsperiod i dagar</span><span class="sxs-lookup"><span data-stu-id="88528-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="88528-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="88528-126">-Slot</span></span>
<span data-ttu-id="88528-127">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="88528-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="88528-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="88528-128">-StartTime</span></span>
<span data-ttu-id="88528-129">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="88528-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="88528-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="88528-130">-StorageAccountUrl</span></span>
<span data-ttu-id="88528-131">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="88528-131">Storage Account Url</span></span>

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

### <span data-ttu-id="88528-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="88528-132">-WebApp</span></span>
<span data-ttu-id="88528-133">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="88528-133">WebApp Object</span></span>

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

### <span data-ttu-id="88528-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88528-134">CommonParameters</span></span>
<span data-ttu-id="88528-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88528-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88528-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88528-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88528-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88528-137">INPUTS</span></span>

### <span data-ttu-id="88528-138">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="88528-138">Site</span></span>
<span data-ttu-id="88528-139">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="88528-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="88528-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88528-140">OUTPUTS</span></span>

### <span data-ttu-id="88528-141">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="88528-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="88528-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88528-142">NOTES</span></span>

## <span data-ttu-id="88528-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88528-143">RELATED LINKS</span></span>

[<span data-ttu-id="88528-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="88528-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


