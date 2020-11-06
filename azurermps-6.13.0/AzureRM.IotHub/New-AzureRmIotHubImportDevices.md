---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubimportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
ms.openlocfilehash: 37445e2f88172c3a9e703c85562518212baa9e83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578015"
---
# <span data-ttu-id="7ae4c-101">New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="7ae4c-101">New-AzureRmIotHubImportDevices</span></span>

## <span data-ttu-id="7ae4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ae4c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae4c-103">Skapar ett nytt import utrustnings jobb.</span><span class="sxs-lookup"><span data-stu-id="7ae4c-103">Creates a new import devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ae4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ae4c-104">SYNTAX</span></span>

```
New-AzureRmIotHubImportDevices [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ae4c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ae4c-105">DESCRIPTION</span></span>
<span data-ttu-id="7ae4c-106">Skapar ett nytt import enheter jobb för IotHub.</span><span class="sxs-lookup"><span data-stu-id="7ae4c-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="7ae4c-107">Detta importerar alla enheter till IotHub från den angivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="7ae4c-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="7ae4c-108">Läs följande artikel om hur du skapar SAS URI.</span><span class="sxs-lookup"><span data-stu-id="7ae4c-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="7ae4c-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="7ae4c-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="7ae4c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ae4c-110">EXAMPLES</span></span>

### <span data-ttu-id="7ae4c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ae4c-111">Example 1</span></span>
```
PS C:\> New-AzureRmIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="7ae4c-112">Skapar en ny begäran om import enhet för IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="7ae4c-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="7ae4c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ae4c-113">PARAMETERS</span></span>

### <span data-ttu-id="7ae4c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae4c-114">-DefaultProfile</span></span>
<span data-ttu-id="7ae4c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7ae4c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ae4c-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="7ae4c-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="7ae4c-117">URI för BLOB-behållare för FileUpload</span><span class="sxs-lookup"><span data-stu-id="7ae4c-117">Input Blob Container Uri for FileUpload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae4c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ae4c-118">-Name</span></span>
<span data-ttu-id="7ae4c-119">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="7ae4c-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="7ae4c-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="7ae4c-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="7ae4c-121">Den URI som utdata ska skrivas till.</span><span class="sxs-lookup"><span data-stu-id="7ae4c-121">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae4c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae4c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7ae4c-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7ae4c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7ae4c-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ae4c-124">-Confirm</span></span>
<span data-ttu-id="7ae4c-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ae4c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae4c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ae4c-126">-WhatIf</span></span>
<span data-ttu-id="7ae4c-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ae4c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ae4c-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ae4c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae4c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae4c-129">CommonParameters</span></span>
<span data-ttu-id="7ae4c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae4c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae4c-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae4c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae4c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ae4c-132">INPUTS</span></span>

### <span data-ttu-id="7ae4c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7ae4c-133">System.String</span></span>

## <span data-ttu-id="7ae4c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ae4c-134">OUTPUTS</span></span>

### <span data-ttu-id="7ae4c-135">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="7ae4c-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="7ae4c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ae4c-136">NOTES</span></span>

## <span data-ttu-id="7ae4c-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ae4c-137">RELATED LINKS</span></span>
