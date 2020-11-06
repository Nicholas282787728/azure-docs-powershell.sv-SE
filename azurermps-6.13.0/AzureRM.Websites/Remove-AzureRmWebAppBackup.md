---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: 98ded2967c364955ab8b9dd38f316021649d0fc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576009"
---
# <span data-ttu-id="11340-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="11340-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="11340-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11340-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11340-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11340-103">SYNTAX</span></span>

### <span data-ttu-id="11340-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="11340-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11340-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="11340-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11340-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11340-106">DESCRIPTION</span></span>
<span data-ttu-id="11340-107">Cmdleten **Remove-AzureRmWebAppBackup** tar bort den angivna säkerhets kopian av ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="11340-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="11340-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11340-108">EXAMPLES</span></span>

### <span data-ttu-id="11340-109">9.1</span><span class="sxs-lookup"><span data-stu-id="11340-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="11340-110">Med det här kommandot tas säkerhets kopian bort med ID för "12345" från webb programmet med namnet WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="11340-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="11340-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11340-111">PARAMETERS</span></span>

### <span data-ttu-id="11340-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="11340-112">-BackupId</span></span>
<span data-ttu-id="11340-113">Säkerhets kopie-ID</span><span class="sxs-lookup"><span data-stu-id="11340-113">Backup Id</span></span>

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

### <span data-ttu-id="11340-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11340-114">-DefaultProfile</span></span>
<span data-ttu-id="11340-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11340-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11340-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="11340-116">-Name</span></span>
<span data-ttu-id="11340-117">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="11340-117">WebApp Name</span></span>

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

### <span data-ttu-id="11340-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11340-118">-ResourceGroupName</span></span>
<span data-ttu-id="11340-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="11340-119">Resource Group Name</span></span>

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

### <span data-ttu-id="11340-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="11340-120">-Slot</span></span>
<span data-ttu-id="11340-121">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="11340-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="11340-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="11340-122">-WebApp</span></span>
<span data-ttu-id="11340-123">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="11340-123">WebApp Object</span></span>

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

### <span data-ttu-id="11340-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11340-124">CommonParameters</span></span>
<span data-ttu-id="11340-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11340-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11340-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11340-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11340-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11340-127">INPUTS</span></span>

### <span data-ttu-id="11340-128">System. String</span><span class="sxs-lookup"><span data-stu-id="11340-128">System.String</span></span>

### <span data-ttu-id="11340-129">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="11340-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="11340-130">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="11340-130">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="11340-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11340-131">OUTPUTS</span></span>

### <span data-ttu-id="11340-132">Microsoft. Azure. Management. webbplatser. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="11340-132">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="11340-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11340-133">NOTES</span></span>

## <span data-ttu-id="11340-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11340-134">RELATED LINKS</span></span>
