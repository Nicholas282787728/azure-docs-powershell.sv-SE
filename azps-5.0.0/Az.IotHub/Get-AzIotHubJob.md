---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319492"
---
# <span data-ttu-id="8b78a-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="8b78a-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="8b78a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b78a-102">SYNOPSIS</span></span>
<span data-ttu-id="8b78a-103">Hämtar information om ett IotHub-jobb.</span><span class="sxs-lookup"><span data-stu-id="8b78a-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="8b78a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b78a-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b78a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b78a-105">DESCRIPTION</span></span>
<span data-ttu-id="8b78a-106">Hämtar information om ett IotHub-jobb.</span><span class="sxs-lookup"><span data-stu-id="8b78a-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="8b78a-107">Ett IotHub-jobb skapas när en import-eller export åtgärd initieras med hjälp av New-AzIotHubExportDevices eller New-AzIotHubImportDevices kommandon.</span><span class="sxs-lookup"><span data-stu-id="8b78a-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="8b78a-108">Du kan antingen Visa alla jobb eller filtrera jobben med jobb-ID.</span><span class="sxs-lookup"><span data-stu-id="8b78a-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="8b78a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b78a-109">EXAMPLES</span></span>

### <span data-ttu-id="8b78a-110">Exempel 1 visar alla jobb</span><span class="sxs-lookup"><span data-stu-id="8b78a-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="8b78a-111">Hämtar alla jobb för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8b78a-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="8b78a-112">Exempel 2 Hämta ett specifikt jobb</span><span class="sxs-lookup"><span data-stu-id="8b78a-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="8b78a-113">Hämtar information om jobbet med identifieraren "3630fc31-4caa-43e8-A232-ea0577221cb2" för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8b78a-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8b78a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b78a-114">PARAMETERS</span></span>

### <span data-ttu-id="8b78a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b78a-115">-DefaultProfile</span></span>
<span data-ttu-id="8b78a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8b78a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b78a-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="8b78a-117">-JobId</span></span>
<span data-ttu-id="8b78a-118">Jobb-ID.</span><span class="sxs-lookup"><span data-stu-id="8b78a-118">The Job Identifier.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b78a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b78a-119">-Name</span></span>
<span data-ttu-id="8b78a-120">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="8b78a-120">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b78a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b78a-121">-ResourceGroupName</span></span>
<span data-ttu-id="8b78a-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8b78a-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b78a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b78a-123">CommonParameters</span></span>
<span data-ttu-id="8b78a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b78a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b78a-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b78a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b78a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b78a-126">INPUTS</span></span>

### <span data-ttu-id="8b78a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8b78a-127">System.String</span></span>

## <span data-ttu-id="8b78a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b78a-128">OUTPUTS</span></span>

### <span data-ttu-id="8b78a-129">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="8b78a-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="8b78a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b78a-130">NOTES</span></span>

## <span data-ttu-id="8b78a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b78a-131">RELATED LINKS</span></span>
