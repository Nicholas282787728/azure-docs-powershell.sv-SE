---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 91a8c53bc8600006a3a57a5dfefb1141652ca3d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573595"
---
# <span data-ttu-id="d878f-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d878f-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="d878f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d878f-102">SYNOPSIS</span></span>
<span data-ttu-id="d878f-103">Stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="d878f-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d878f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d878f-104">SYNTAX</span></span>

### <span data-ttu-id="d878f-105">S</span><span class="sxs-lookup"><span data-stu-id="d878f-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d878f-106">S2</span><span class="sxs-lookup"><span data-stu-id="d878f-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d878f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d878f-107">DESCRIPTION</span></span>
<span data-ttu-id="d878f-108">Cmdleten **Stop-AzureRmWebAppSlot** stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="d878f-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="d878f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d878f-109">EXAMPLES</span></span>

### <span data-ttu-id="d878f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d878f-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="d878f-111">Det här kommandot stoppar fack Slot001 för webb programmet som heter ContosoWebApp som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="d878f-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d878f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d878f-112">PARAMETERS</span></span>

### <span data-ttu-id="d878f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d878f-113">-Name</span></span>
<span data-ttu-id="d878f-114">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d878f-114">WebApp Name</span></span>

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

### <span data-ttu-id="d878f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d878f-115">-ResourceGroupName</span></span>
<span data-ttu-id="d878f-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d878f-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d878f-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="d878f-117">-Slot</span></span>
<span data-ttu-id="d878f-118">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="d878f-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d878f-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d878f-119">-WebApp</span></span>
<span data-ttu-id="d878f-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="d878f-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d878f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d878f-121">-DefaultProfile</span></span>
<span data-ttu-id="d878f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d878f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d878f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d878f-123">CommonParameters</span></span>
<span data-ttu-id="d878f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d878f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d878f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d878f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d878f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d878f-126">INPUTS</span></span>

### <span data-ttu-id="d878f-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="d878f-127">Site</span></span>
<span data-ttu-id="d878f-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d878f-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d878f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d878f-129">OUTPUTS</span></span>

## <span data-ttu-id="d878f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d878f-130">NOTES</span></span>

## <span data-ttu-id="d878f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d878f-131">RELATED LINKS</span></span>

