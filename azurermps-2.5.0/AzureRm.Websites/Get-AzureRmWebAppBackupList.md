---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
ms.openlocfilehash: ef409c62d56a95d36f1e7c9a02018b281c00e3c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929194"
---
# <span data-ttu-id="217f4-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="217f4-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="217f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="217f4-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="217f4-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="217f4-103">SYNTAX</span></span>

### <span data-ttu-id="217f4-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="217f4-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="217f4-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="217f4-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="217f4-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="217f4-106">DESCRIPTION</span></span>
<span data-ttu-id="217f4-107">Cmdleten **Get-AzureRmWebAppBackupList** hämtar en lista över säkerhets kopior för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="217f4-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="217f4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="217f4-108">EXAMPLES</span></span>

### <span data-ttu-id="217f4-109">9.1</span><span class="sxs-lookup"><span data-stu-id="217f4-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="217f4-110">Det här kommandot returnerar en säkerhets kopierings lista som hör till WebApp-WebAppStandard som är kopplad till resurs grupps ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="217f4-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="217f4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="217f4-111">PARAMETERS</span></span>

### <span data-ttu-id="217f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217f4-112">-DefaultProfile</span></span>
<span data-ttu-id="217f4-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="217f4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="217f4-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="217f4-114">-Name</span></span>
<span data-ttu-id="217f4-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="217f4-115">WebApp Name</span></span>

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

### <span data-ttu-id="217f4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="217f4-116">-ResourceGroupName</span></span>
<span data-ttu-id="217f4-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="217f4-117">Resource Group Name</span></span>

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

### <span data-ttu-id="217f4-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="217f4-118">-Slot</span></span>
<span data-ttu-id="217f4-119">Plats namn</span><span class="sxs-lookup"><span data-stu-id="217f4-119">Slot name</span></span>

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

### <span data-ttu-id="217f4-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="217f4-120">-WebApp</span></span>
<span data-ttu-id="217f4-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="217f4-121">Piped WebApp</span></span>

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

### <span data-ttu-id="217f4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217f4-122">CommonParameters</span></span>
<span data-ttu-id="217f4-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="217f4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217f4-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="217f4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217f4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="217f4-125">INPUTS</span></span>

### <span data-ttu-id="217f4-126">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="217f4-126">Site</span></span>
<span data-ttu-id="217f4-127">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="217f4-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="217f4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="217f4-128">OUTPUTS</span></span>

### <span data-ttu-id="217f4-129">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="217f4-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="217f4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="217f4-130">NOTES</span></span>

## <span data-ttu-id="217f4-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="217f4-131">RELATED LINKS</span></span>

