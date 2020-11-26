---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 3b04e0598897fb206ca781f4f19d9e8e2ec206dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273482"
---
# <span data-ttu-id="3958e-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="3958e-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="3958e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3958e-102">SYNOPSIS</span></span>
<span data-ttu-id="3958e-103">Skapar ett nytt export enheter jobb.</span><span class="sxs-lookup"><span data-stu-id="3958e-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="3958e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3958e-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3958e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3958e-105">DESCRIPTION</span></span>
<span data-ttu-id="3958e-106">Skapar ett nytt export enheter jobb för IotHub.</span><span class="sxs-lookup"><span data-stu-id="3958e-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="3958e-107">Då exporteras alla enheter till den angivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="3958e-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="3958e-108">Läs följande artikel om hur du skapar SAS URI.</span><span class="sxs-lookup"><span data-stu-id="3958e-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="3958e-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="3958e-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="3958e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3958e-110">EXAMPLES</span></span>

### <span data-ttu-id="3958e-111">Exempel 1 skickar en begäran om export enhet.</span><span class="sxs-lookup"><span data-stu-id="3958e-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="3958e-112">Skapar en ny begäran om export enhet för IotHub "myiothub" Förutom nycklarna.</span><span class="sxs-lookup"><span data-stu-id="3958e-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="3958e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3958e-113">PARAMETERS</span></span>

### <span data-ttu-id="3958e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3958e-114">-DefaultProfile</span></span>
<span data-ttu-id="3958e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3958e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3958e-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="3958e-116">-ExcludeKeys</span></span>
<span data-ttu-id="3958e-117">Gör det möjligt att exportera enheter utan nycklar.</span><span class="sxs-lookup"><span data-stu-id="3958e-117">Allows to export devices without keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3958e-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="3958e-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="3958e-119">URI som du vill exportera blobben till.</span><span class="sxs-lookup"><span data-stu-id="3958e-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="3958e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3958e-120">-Name</span></span>
<span data-ttu-id="3958e-121">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="3958e-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="3958e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3958e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3958e-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3958e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="3958e-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3958e-124">-Confirm</span></span>
<span data-ttu-id="3958e-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3958e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3958e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3958e-126">-WhatIf</span></span>
<span data-ttu-id="3958e-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3958e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3958e-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3958e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3958e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3958e-129">CommonParameters</span></span>
<span data-ttu-id="3958e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3958e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3958e-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3958e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3958e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3958e-132">INPUTS</span></span>

### <span data-ttu-id="3958e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3958e-133">System.String</span></span>

## <span data-ttu-id="3958e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3958e-134">OUTPUTS</span></span>

### <span data-ttu-id="3958e-135">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="3958e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="3958e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3958e-136">NOTES</span></span>

## <span data-ttu-id="3958e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3958e-137">RELATED LINKS</span></span>