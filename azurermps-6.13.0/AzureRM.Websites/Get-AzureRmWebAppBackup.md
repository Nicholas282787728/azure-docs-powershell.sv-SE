---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: 7b3e721adaa0389f1c2a75750d7bf36dfe4c2ac1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755181"
---
# <span data-ttu-id="e9f8e-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e9f8e-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="e9f8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9f8e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9f8e-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9f8e-103">SYNTAX</span></span>

### <span data-ttu-id="e9f8e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e9f8e-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9f8e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e9f8e-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9f8e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9f8e-106">DESCRIPTION</span></span>
<span data-ttu-id="e9f8e-107">Cmdleten **Get-AzureRmWebAppBackup** hämtar den angivna säkerhets kopian av ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e9f8e-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="e9f8e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9f8e-108">EXAMPLES</span></span>

### <span data-ttu-id="e9f8e-109">9.1</span><span class="sxs-lookup"><span data-stu-id="e9f8e-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="e9f8e-110">Med det här kommandot får du säkerhets kopian med ID: t "12345" från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="e9f8e-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e9f8e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9f8e-111">PARAMETERS</span></span>

### <span data-ttu-id="e9f8e-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="e9f8e-112">-BackupId</span></span>
<span data-ttu-id="e9f8e-113">Säkerhets kopie-ID</span><span class="sxs-lookup"><span data-stu-id="e9f8e-113">Backup Id</span></span>

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

### <span data-ttu-id="e9f8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f8e-114">-DefaultProfile</span></span>
<span data-ttu-id="e9f8e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9f8e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9f8e-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9f8e-116">-Name</span></span>
<span data-ttu-id="e9f8e-117">Webapp-namn</span><span class="sxs-lookup"><span data-stu-id="e9f8e-117">Webapp Name</span></span>

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

### <span data-ttu-id="e9f8e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f8e-118">-ResourceGroupName</span></span>
<span data-ttu-id="e9f8e-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e9f8e-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e9f8e-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="e9f8e-120">-Slot</span></span>
<span data-ttu-id="e9f8e-121">Plats namn</span><span class="sxs-lookup"><span data-stu-id="e9f8e-121">Slot Name</span></span>

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

### <span data-ttu-id="e9f8e-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e9f8e-122">-WebApp</span></span>
<span data-ttu-id="e9f8e-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="e9f8e-123">Piped WebApp</span></span>

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

### <span data-ttu-id="e9f8e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f8e-124">CommonParameters</span></span>
<span data-ttu-id="e9f8e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f8e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f8e-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f8e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f8e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9f8e-127">INPUTS</span></span>

### <span data-ttu-id="e9f8e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e9f8e-128">System.String</span></span>

### <span data-ttu-id="e9f8e-129">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="e9f8e-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="e9f8e-130">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e9f8e-130">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="e9f8e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9f8e-131">OUTPUTS</span></span>

### <span data-ttu-id="e9f8e-132">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e9f8e-132">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="e9f8e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9f8e-133">NOTES</span></span>

## <span data-ttu-id="e9f8e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9f8e-134">RELATED LINKS</span></span>
