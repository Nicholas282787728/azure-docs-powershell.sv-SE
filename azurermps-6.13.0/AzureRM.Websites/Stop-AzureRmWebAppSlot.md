---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 2e6130b93a3c549ca84c2cb0a6a336f6afb177b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576719"
---
# <span data-ttu-id="f8e21-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8e21-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="f8e21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8e21-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e21-103">Stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="f8e21-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8e21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8e21-104">SYNTAX</span></span>

### <span data-ttu-id="f8e21-105">S</span><span class="sxs-lookup"><span data-stu-id="f8e21-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8e21-106">S2</span><span class="sxs-lookup"><span data-stu-id="f8e21-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8e21-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8e21-107">DESCRIPTION</span></span>
<span data-ttu-id="f8e21-108">Cmdleten **Stop-AzureRmWebAppSlot** stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="f8e21-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="f8e21-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8e21-109">EXAMPLES</span></span>

### <span data-ttu-id="f8e21-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f8e21-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="f8e21-111">Det här kommandot stoppar fack Slot001 för webb programmet som heter ContosoWebApp som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="f8e21-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f8e21-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8e21-112">PARAMETERS</span></span>

### <span data-ttu-id="f8e21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e21-113">-DefaultProfile</span></span>
<span data-ttu-id="f8e21-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e21-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8e21-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8e21-115">-Name</span></span>
<span data-ttu-id="f8e21-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="f8e21-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8e21-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e21-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8e21-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="f8e21-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e21-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="f8e21-119">-Slot</span></span>
<span data-ttu-id="f8e21-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="f8e21-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e21-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f8e21-121">-WebApp</span></span>
<span data-ttu-id="f8e21-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="f8e21-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8e21-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e21-123">CommonParameters</span></span>
<span data-ttu-id="f8e21-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8e21-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e21-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e21-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e21-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8e21-126">INPUTS</span></span>

### <span data-ttu-id="f8e21-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f8e21-127">System.String</span></span>

### <span data-ttu-id="f8e21-128">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="f8e21-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="f8e21-129">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f8e21-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="f8e21-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8e21-130">OUTPUTS</span></span>

### <span data-ttu-id="f8e21-131">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="f8e21-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="f8e21-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8e21-132">NOTES</span></span>

## <span data-ttu-id="f8e21-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8e21-133">RELATED LINKS</span></span>
