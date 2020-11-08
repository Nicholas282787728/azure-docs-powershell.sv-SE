---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: a53f67c12a5c8d125319fc19f69db3ea9a57c5e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091113"
---
# <span data-ttu-id="b4817-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b4817-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="b4817-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4817-102">SYNOPSIS</span></span>
<span data-ttu-id="b4817-103">Skapar en ny användare för enheten.</span><span class="sxs-lookup"><span data-stu-id="b4817-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="b4817-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4817-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4817-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4817-105">DESCRIPTION</span></span>
<span data-ttu-id="b4817-106">Den **nya AzDataBoxEdgeUser-** cmdleten skapar en ny användare för data Box Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="b4817-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="b4817-107">Det går bara att skapa en typ av användare `Share` .</span><span class="sxs-lookup"><span data-stu-id="b4817-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="b4817-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4817-108">EXAMPLES</span></span>

### <span data-ttu-id="b4817-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4817-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="b4817-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4817-110">PARAMETERS</span></span>

### <span data-ttu-id="b4817-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4817-111">-AsJob</span></span>
<span data-ttu-id="b4817-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b4817-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4817-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4817-113">-DefaultProfile</span></span>
<span data-ttu-id="b4817-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4817-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4817-115">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="b4817-115">-DeviceName</span></span>
<span data-ttu-id="b4817-116">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="b4817-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4817-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b4817-117">-EncryptionKey</span></span>
<span data-ttu-id="b4817-118">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="b4817-118">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4817-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4817-119">-Name</span></span>
<span data-ttu-id="b4817-120">Namnen</span><span class="sxs-lookup"><span data-stu-id="b4817-120">Username</span></span>

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

### <span data-ttu-id="b4817-121">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="b4817-121">-Password</span></span>
<span data-ttu-id="b4817-122">Lösen ord, ange som en säker sträng</span><span class="sxs-lookup"><span data-stu-id="b4817-122">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4817-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4817-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4817-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b4817-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4817-125">– Skriv</span><span class="sxs-lookup"><span data-stu-id="b4817-125">-Type</span></span>
<span data-ttu-id="b4817-126">Välj UserType</span><span class="sxs-lookup"><span data-stu-id="b4817-126">Select UserType</span></span>

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

### <span data-ttu-id="b4817-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4817-127">-Confirm</span></span>
<span data-ttu-id="b4817-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4817-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4817-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4817-129">-WhatIf</span></span>
<span data-ttu-id="b4817-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4817-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4817-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4817-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4817-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4817-132">CommonParameters</span></span>
<span data-ttu-id="b4817-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4817-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4817-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4817-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4817-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4817-135">INPUTS</span></span>

### <span data-ttu-id="b4817-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="b4817-136">None</span></span>

## <span data-ttu-id="b4817-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4817-137">OUTPUTS</span></span>

### <span data-ttu-id="b4817-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b4817-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b4817-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4817-139">NOTES</span></span>

## <span data-ttu-id="b4817-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4817-140">RELATED LINKS</span></span>