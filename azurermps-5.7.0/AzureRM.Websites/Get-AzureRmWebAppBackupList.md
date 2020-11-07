---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: 0f8192441b3bf555145da8259f369a9091193800
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755364"
---
# <span data-ttu-id="5e999-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="5e999-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="5e999-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e999-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e999-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e999-103">SYNTAX</span></span>

### <span data-ttu-id="5e999-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5e999-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e999-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5e999-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e999-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e999-106">DESCRIPTION</span></span>
<span data-ttu-id="5e999-107">Cmdleten **Get-AzureRmWebAppBackupList** hämtar en lista över säkerhets kopior för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5e999-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="5e999-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e999-108">EXAMPLES</span></span>

### <span data-ttu-id="5e999-109">9.1</span><span class="sxs-lookup"><span data-stu-id="5e999-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="5e999-110">Det här kommandot returnerar en säkerhets kopierings lista som hör till WebApp-WebAppStandard som är kopplad till resurs grupps ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5e999-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="5e999-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e999-111">PARAMETERS</span></span>

### <span data-ttu-id="5e999-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e999-112">-DefaultProfile</span></span>
<span data-ttu-id="5e999-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e999-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e999-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e999-114">-Name</span></span>
<span data-ttu-id="5e999-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="5e999-115">WebApp Name</span></span>

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

### <span data-ttu-id="5e999-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e999-116">-ResourceGroupName</span></span>
<span data-ttu-id="5e999-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5e999-117">Resource Group Name</span></span>

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

### <span data-ttu-id="5e999-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="5e999-118">-Slot</span></span>
<span data-ttu-id="5e999-119">Plats namn</span><span class="sxs-lookup"><span data-stu-id="5e999-119">Slot name</span></span>

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

### <span data-ttu-id="5e999-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5e999-120">-WebApp</span></span>
<span data-ttu-id="5e999-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="5e999-121">Piped WebApp</span></span>

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

### <span data-ttu-id="5e999-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e999-122">CommonParameters</span></span>
<span data-ttu-id="5e999-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e999-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e999-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e999-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e999-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e999-125">INPUTS</span></span>

### <span data-ttu-id="5e999-126">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="5e999-126">Site</span></span>
<span data-ttu-id="5e999-127">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5e999-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5e999-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e999-128">OUTPUTS</span></span>

### <span data-ttu-id="5e999-129">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="5e999-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="5e999-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e999-130">NOTES</span></span>

## <span data-ttu-id="5e999-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e999-131">RELATED LINKS</span></span>

