---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: daacefe94d694a6d6288e4c1ccd0f6b05ad1e582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577198"
---
# <span data-ttu-id="1d44c-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="1d44c-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="1d44c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d44c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d44c-103">Hämtar information om ett IotHub-jobb.</span><span class="sxs-lookup"><span data-stu-id="1d44c-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d44c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d44c-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d44c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d44c-105">DESCRIPTION</span></span>
<span data-ttu-id="1d44c-106">Hämtar information om ett IotHub-jobb.</span><span class="sxs-lookup"><span data-stu-id="1d44c-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="1d44c-107">Ett IotHub-jobb skapas när en import-eller export åtgärd utförs med New-AzureRmIotHubExportDevices eller New-AzureRmIotHubImportDevices kommandon.</span><span class="sxs-lookup"><span data-stu-id="1d44c-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="1d44c-108">Du kan antingen Visa alla jobb eller filtrera jobben med jobb-ID.</span><span class="sxs-lookup"><span data-stu-id="1d44c-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="1d44c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d44c-109">EXAMPLES</span></span>

### <span data-ttu-id="1d44c-110">Exempel 1 visar alla jobb</span><span class="sxs-lookup"><span data-stu-id="1d44c-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1d44c-111">Hämtar alla jobb för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="1d44c-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="1d44c-112">Exempel 2 Hämta ett specifikt jobb</span><span class="sxs-lookup"><span data-stu-id="1d44c-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="1d44c-113">Hämtar information om jobbet med identifieraren "3630fc31-4caa-43e8-A232-ea0577221cb2" för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="1d44c-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="1d44c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d44c-114">PARAMETERS</span></span>

### <span data-ttu-id="1d44c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d44c-115">-DefaultProfile</span></span>
<span data-ttu-id="1d44c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1d44c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d44c-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="1d44c-117">-JobId</span></span>
<span data-ttu-id="1d44c-118">Jobb-ID.</span><span class="sxs-lookup"><span data-stu-id="1d44c-118">The Job Identifier.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d44c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d44c-119">-Name</span></span>
<span data-ttu-id="1d44c-120">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="1d44c-120">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d44c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d44c-121">-ResourceGroupName</span></span>
<span data-ttu-id="1d44c-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1d44c-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d44c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d44c-123">CommonParameters</span></span>
<span data-ttu-id="1d44c-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d44c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d44c-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d44c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d44c-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d44c-126">INPUTS</span></span>

### <span data-ttu-id="1d44c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1d44c-127">System.String</span></span>

## <span data-ttu-id="1d44c-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d44c-128">OUTPUTS</span></span>

### <span data-ttu-id="1d44c-129">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="1d44c-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>
<span data-ttu-id="1d44c-130">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. kommandon. Management. IotHub. Models. PSIotHubJobResponse, Microsoft. Azure. commands. IotHub, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="1d44c-130">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="1d44c-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d44c-131">NOTES</span></span>

## <span data-ttu-id="1d44c-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d44c-132">RELATED LINKS</span></span>

