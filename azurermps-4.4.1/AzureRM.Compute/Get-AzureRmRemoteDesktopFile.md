---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: 9e546815c7333bf468a204c6a22f9426c24b65d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575007"
---
# <span data-ttu-id="1f0f2-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="1f0f2-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="1f0f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="1f0f2-103">Hämtar en. RDP-fil.</span><span class="sxs-lookup"><span data-stu-id="1f0f2-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f0f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f0f2-104">SYNTAX</span></span>

### <span data-ttu-id="1f0f2-105">Bar</span><span class="sxs-lookup"><span data-stu-id="1f0f2-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f0f2-106">Start</span><span class="sxs-lookup"><span data-stu-id="1f0f2-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f0f2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f0f2-107">DESCRIPTION</span></span>
<span data-ttu-id="1f0f2-108">Cmdleten **Get-AzureRmRemoteDesktopFile** hämtar en RDP-fil (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="1f0f2-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="1f0f2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f0f2-109">EXAMPLES</span></span>

### <span data-ttu-id="1f0f2-110">Exempel 1: Hämta en fjärr skrivbords fil</span><span class="sxs-lookup"><span data-stu-id="1f0f2-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="1f0f2-111">Det här kommandot får fjärr skrivbords filen för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="1f0f2-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="1f0f2-112">Kommandot sparar resultatet i filen med namnet D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="1f0f2-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="1f0f2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f0f2-113">PARAMETERS</span></span>

### <span data-ttu-id="1f0f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f0f2-114">-DefaultProfile</span></span>
<span data-ttu-id="1f0f2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f0f2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f0f2-116">-Lansera</span><span class="sxs-lookup"><span data-stu-id="1f0f2-116">-Launch</span></span>
<span data-ttu-id="1f0f2-117">Anger att denna cmdlet startar fjärr skrivbord när den får. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="1f0f2-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f0f2-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="1f0f2-118">-LocalPath</span></span>
<span data-ttu-id="1f0f2-119">Anger lokal fullständig sökväg där denna cmdlet lagrar. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="1f0f2-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f0f2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f0f2-120">-Name</span></span>
<span data-ttu-id="1f0f2-121">Anger namnet på den tillgänglighets uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="1f0f2-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f0f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f0f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f0f2-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1f0f2-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1f0f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f0f2-124">CommonParameters</span></span>
<span data-ttu-id="1f0f2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f0f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f0f2-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f0f2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f0f2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f0f2-127">INPUTS</span></span>

## <span data-ttu-id="1f0f2-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f0f2-128">OUTPUTS</span></span>

## <span data-ttu-id="1f0f2-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f0f2-129">NOTES</span></span>

## <span data-ttu-id="1f0f2-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f0f2-130">RELATED LINKS</span></span>

